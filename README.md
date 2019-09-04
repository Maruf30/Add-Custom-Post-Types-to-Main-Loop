# Add-Custom-Post-Types-to-Main-Loop

function add_to_main_loop($query) {
    if ($query->is_main_query()) {
        $query->set('post_type', array('post','POST_TYPE'));
    }
}
  
add_action('pre_get_posts', 'add_to_main_loop');
