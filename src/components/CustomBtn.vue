<template>
  <button class="btn" :class="{
    'btn--hover': hover && variant === 'default',
    'btn--sm': size === 'sm',
    'btn--md': size === 'md',
    'btn--lg': size === 'lg',
    'btn--default': color === 'default',
    'btn--primary': color === 'primary',
    'btn--secondary': color === 'secondary',
    'btn--danger': color === 'danger',
    'btn--default--hover': color === 'default' && hover,
    'btn--primary--hover': color === 'primary' && hover,
    'btn--secondary--hover': color === 'secondary' && hover,
    'btn--danger--hover': color === 'danger' && hover === 'true',
    'btn--outlined': variant === 'outlined',
    'btn--outlined--hover': hover && variant === 'outlined' && !disabled,
    'btn--text': variant === 'text',
    'btn--text--hover': hover && variant === 'text' && !disabled,
    'btn--text--disabled': disabled && variant === 'text',
    'btn--disableShadow': disableShadow,
    'btn--disabled': disabled,
  }">
    <span v-show="startIcon" class="material-icons-outlined icon"> {{ startIcon }}</span>
    {{ text }}
    <span v-show="endIcon" class="material-icons-outlined icon">{{ endIcon }}</span>
  </button>
</template>

<script>
export default {
  props: {
    'text': {
      type: String,
      default: 'Default'
    },
    'variant': {
      type: String,
      default: 'default'
    },
    'hover': {
      type: Boolean,
      default: false
    },
    'disableShadow': {
      type: Boolean,
      default: false
    },
    'disabled': {
      type: Boolean,
      default: false
    },
    'startIcon': String,
    'endIcon': String,
    'size': {
      type: String,
      default: 'md'
    },
    'color': {
      type: String,
      default: 'default'
    }},
}

</script>

<style lang="scss" scoped>
$primary: #2962FF;
$secondary: #455A64;
$danger: #D32F2F;

.btn {
  display: flex;
  align-items: center;

  border-radius: 6px;

  font-family: 'Noto Sans JP', sans-serif;

  &--sm {
    padding: 6px 12px;
  }

  &--md {
    padding: 8px 16px;
  }

  &--lg {
    padding: 11px 22px;
  }

  &--default {
    background: #E0E0E0;
    box-shadow: 0 2px 3px rgba(51, 51, 51, 0.2);
    color: #3F3F3F;

    &--hover {
      background: #AEAEAE;
    }
  }

  &--primary {
    background: $primary;
    color: #ffffff;
    box-shadow: 0 2px 3px rgba(41, 98, 255, 0.2);

    &--hover {
      background: #0039CB;
      box-shadow: 0px 2px 3px rgba(41, 98, 255, 0.2);
    }
  }

  &--secondary {
    background: $secondary;
    color: #ffffff;

    &--hover {
      background: #1C313A;
    }
  }

  &--danger {
    background: $danger;
    color: #ffffff;
    box-shadow: 0 2px 3px rgba(211, 47, 47, 0.2);

    &--hover {
      background: #9A0007;
    }
  }

  span:first-child {
    margin-right: 10px;
  }

  span:last-child {
    margin-left: 10px;
  }

  .icon {
    font-size: 19px;
  }

  &--outlined {
    border: 1px solid #3D5AFE;
    color: #3D5AFE;
    background: #ffffff;
    box-shadow: none;

    &--hover {
      background: rgba(41, 98, 255, 0.1);
      box-shadow: none;
    }
  }

  &--text {
    border: none;
    background: none;
    box-shadow: none;

    color: #3D5AFE;

    padding: 8px 0;

    &--hover {
      padding: 8px 16px;
      background: rgba(41, 98, 255, 0.1);
      border-radius: 6px;
      box-shadow: none;
      color: #3D5AFE;
    }

    &--disabled {
      color: #9E9E9E !important;
      background: #ffffff !important;
      padding: 8px 0 !important;
    }
  }

  &--disableShadow {
    box-shadow: none;
  }

  &--disabled {
    background: #E0E0E0;
    color: #9E9E9E;
  }
}
</style>