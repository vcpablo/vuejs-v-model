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
        Custom Prop and Event
      </legend>
        <BaseInputCustomPropAndEvent v-model="customPropAndEventText" />
        <p>
          Value: {{ customPropAndEventText }}
        </p>
    </fieldset>
     <fieldset>
      <legend>
        The ".sync" modifier
      </legend>
        <BaseInputSyncModifier :text.sync="syncModifierText" />
        <p>
          Value: {{ syncModifierText }}
        </p>
    </fieldset>
  </div>
</template>

<script>
import BaseInputLocalVariableWatcher from './components/BaseInputLocalVariableWatcher'
import BaseInputCustomMethod from './components/BaseInputCustomMethod'
import BaseInputPowerfulComputedProperty from './components/BaseInputPowerfulComputedProperty'
import BaseInputCustomPropAndEvent from './components/BaseInputCustomPropAndEvent'
import BaseInputSyncModifier from './components/BaseInputSyncModifier'

export default {
  name: 'App',
  components: {
    BaseInputLocalVariableWatcher,
    BaseInputCustomMethod,
    BaseInputPowerfulComputedProperty,
    BaseInputCustomPropAndEvent,
    BaseInputSyncModifier
  },
  data() {
    return {
      localVariableWatcherText: '',
      customMethodText: '',
      powerfulComputedPropertyText: '',
      customPropAndEventText: '',
      syncModifierText: ''
    }
  }
}
</script>
