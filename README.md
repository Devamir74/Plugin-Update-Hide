function disable_plugin_updates($value) {
    if (isset($value) && is_object($value)) {
        unset($value->response);
    }
    return $value;
}
add_filter('site_transient_update_plugins', 'disable_plugin_updates');
