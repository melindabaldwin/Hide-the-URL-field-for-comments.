# Hide-the-URL-field-for-comments.
Hide the URL field for comments.
// Remove website field in comments
add_action('comment_form_default_fields', 'remove_website_comment_field');
function remove_website_comment_field($fields)
{
    if (isset($fields['url'])) {
        unset($fields['url']);
    }
    return $fields;
}
