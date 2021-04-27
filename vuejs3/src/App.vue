<template>
  <div>
    <fieldset>
      <legend>
        Local Variable Watcher
      </legend>
        <BaseInputLocalVariableWatcher v-model="localVariableWatcherText" />
        <p>
          Value: {{ localVariableWatcherText }}
        </p>
    </fieldset>
    <fieldset>
      <legend>
        Custom Method
      </legend>
        <BaseInputCustomMethod v-model="customMethodText" />
        <p>
          Value: {{ customMethodText }}
        </p>
    </fieldset>
    <fieldset>
      <legend>
        Powerful Computed Property
      </legend>
        <BaseInputPowerfulComputedProperty v-model="powerfulComputedPropertyText" />
        <p>
          Value: {{ powerfulComputedPropertyText }}
        </p>
    </fieldset>
     <fieldset>
      <legend>
        Named v-model
      </legend>
        <BaseInputNamedVModel v-model:text="namedVModelText" />
        <p>
          Value: {{ namedVModelText }}
        </p>
    </fieldset>
  </div>
</template>

<script>
import BaseInputLocalVariableWatcher from './components/BaseInputLocalVariableWatcher'
import BaseInputCustomMethod from './components/BaseInputCustomMethod'
import BaseInputPowerfulComputedProperty from './components/BaseInputPowerfulComputedProperty'
import BaseInputNamedVModel from './components/BaseInputNamedVModel'

export default {
  name: 'App',
  components: {
    BaseInputLocalVariableWatcher,
    BaseInputCustomMethod,
    BaseInputPowerfulComputedProperty,
    // BaseInputCustomPropAndEvent,
    BaseInputNamedVModel
  },
  data() {
    return {
      localVariableWatcherText: '',
      customMethodText: '',
      powerfulComputedPropertyText: '',
      customPropAndEventText: '',
      namedVModelText: ''
    }
  }
}
</script>
