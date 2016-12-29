[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://beta.webcomponents.org/element/jaysunsyn/polymer-tinymce)

# polymer-tinymce

A tinymce HTML Editor as an Polymer Element.

```
<polymer-tinymce on-tiny-chagne="onChange" id="editor"
      tinytoolbar="insertfile undo redo | styleselect | bold italic | alignleft aligncenter alignright alignjustify | bullist numlist outdent indent | link image" 
      tinyplugins='["advlist autolink lists link image charmap print preview anchor","searchreplace visualblocks code fullscreen","insertdatetime media table contextmenu paste"]'
></polymer-tinymce>
```

Get and set content:

```
<script>
    Polymer({

        is: "demo-element",
        properties:{
            value: {type: String, notify: true }
        },

        getContent:function(){
          this.$.contentInput.value = this.$.editor.getContent();
        },

        setContent:function(){
          this.$.editor.setContent(this.$.contentInput.value);
        },
        
        onChange: function(e){
          // Get content
          var content = this.$.editor.getContent();
          // Set local value property with changed content, to be refelcted upwards through data-binding
          this.set('value', content);
        }

      });
</script>
```


[Demo](http://jaysunsyn.github.io/polymer-tinymce)
