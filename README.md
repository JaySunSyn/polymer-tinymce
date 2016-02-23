# polymer-tinymce

A tinymce HTML Editor as an Polymer Element.

```
<polymer-tinymce id="editor"
      tinytoolbar="insertfile undo redo | styleselect | bold italic | alignleft aligncenter alignright alignjustify | bullist numlist outdent indent | link image" 
      tinyplugins='["advlist autolink lists link image charmap print preview anchor","searchreplace visualblocks code fullscreen","insertdatetime media table contextmenu paste"]'
></polymer-tinymce>
```

Get and set content:

```
<script>
    Polymer({

        is: "demo-element",

        getContent:function(){
          this.$.contentInput.value = this.$.editor.getContent();
        },

        setContent:function(){
          this.$.editor.setContent(this.$.contentInput.value);
        }

      });
</script>
```

![Demo Pic](http://www.synappses.com/wp-content/uploads/2015/06/tinymceDemo.png "Polymer-Tinymce")

[Demo](http://jaysunsyn.github.io/polymer-tinymce)
