<script>
    import MaskInput from "svelte-input-mask";

    let mask = "(00) 0 0000-0000";

</script>

<MaskInput {...$$props} alwaysShowMask maskChar="*" {mask}  />
