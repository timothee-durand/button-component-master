<template>
    <button :type="type" :class="classButton" :disabled="disabled">
      <i v-if="startIcon !== ''" class="material-icons icon icon-start" v-html="startIcon"></i>
      <slot>
        Default
      </slot>
      <i v-if="endIcon !== ''" class="material-icons icon icon-end" v-html="endIcon"></i>
    </button>
</template>

<script>
export default {
  name: "Button",
  props: {
    type: {
      type: String,
      default: "button"
    },
    variant:{
      type:String,
      default: "",
    },
    forceHoverFocus: {
      type: Boolean,
      default:false
    },
    disableShadow:{
      type: Boolean,
      default:false
    },
    disabled:{
      type: Boolean,
      default:false
    },
    endIcon:{
      type:String,
      default:"",
    },
    startIcon:{
      type:String,
      default:"",
    },
    size: {
      type:String,
      default:"md"
    },
    color:{
      type:String,
      default:"default"
    }
  },
  computed: {
    classButton() {
      return {
        "outline":this.variant === "outline",
        "text":this.variant === "text",
        "force-hover-focus": this.forceHoverFocus,
        "no-shadow":this.disableShadow,
        "sm":this.size ==="sm",
        "md":this.size ==="md",
        "lg":this.size ==="lg",
        "default":this.color ==="default",
        "primary":this.color ==="primary",
        "secondary":this.color ==="secondary",
        "danger":this.color ==="danger",
      };
    }
  },
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@500&display=swap');
@import url("https://pagecdn.io/lib/normalize/8.0.1/normalize.min.css");
@import url("https://fonts.googleapis.com/icon?family=Material+Icons");

button {
  font-family: 'Noto Sans JP', sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
  text-align: center;

  box-shadow: 0 2px 3px rgba(51, 51, 51, 0.2);
  border-radius: 6px;
  appearance: auto;
  -webkit-writing-mode: horizontal-tb !important;
  text-rendering: auto;
  letter-spacing: normal;
  word-spacing: normal;
  text-transform: none;
  text-indent: 0;
  text-shadow: none;
  cursor: default;
  box-sizing: border-box;
  margin: 0;
  border: none;
  display: flex;
  justify-content: center;
  align-items: center;
  width: max-content;
  transition:all ease 300ms;
}

.icon {
  font-size: 13px;
  display: block;
}

.icon-end {
  margin-left: 6px ;
}
.icon-start{
  margin-right: 6px ;
}

button.outline:hover, button.outline:focus, button.outline.force-hover-focus,
button.text:hover, button.text:focus, button.text.force-hover-focus  {
  background: rgba(41, 98, 255, 0.1);
}

button.text, button[disabled].text {
  background: transparent;
  border: none;
  color: #3D5AFE;
}

button.no-shadow {
  box-shadow: none;
}

button[disabled] {
  background: #E0E0E0;
  border-radius: 6px;
  color: #9E9E9E;
}

button[disabled].text {
  color: #9E9E9E;
  box-shadow: none;
}

button.sm {
  padding:  6px 12px;
}

button.md {
  padding:  8px 16px;
}

button.lg {
  padding:  11px 22px;
}

button.outline {
  background: transparent !important;
}

button.default {
  color: #3F3F3F;
  background-color: #E0E0E0;
}

button.outline.default {
  border: 1px solid #3F3F3F;
  color: #3F3F3F;
}

button.primary {
  background: #2962FF;
  color:white;
}

button.outline.primary {
  border: 1px solid #2962FF;
  color: #2962FF;
}

button.secondary {
  background: #455A64;
  color:white;
}

button.outline.primary {
  border: 1px solid #455A64;
  color: #455A64;
}

button.danger {
  background: #D32F2F;
  color:white;
}

button.outline.danger {
  border: 1px solid #D32F2F;
  color: #D32F2F;
}

button:hover, button:focus, button.force-hover-focus {
  outline: none;
}

button.default:hover, button.default:focus, button.default.force-hover-focus {
  background: #AEAEAE;
}

button.primary:hover, button.primary:focus, button.primary.force-hover-focus {
  background: #0039CB;
}

button.secondary:hover, button.secondary:focus, button.secondary.force-hover-focus {
  background: #1C313A;
}

button.danger:hover, button.danger:focus, button.danger.force-hover-focus {
  background: #9A0007;
}


</style>
