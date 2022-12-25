# wp-codestar-framework
wp-codestar-framework

Example Using:

<pre>
if( class_exists( 'CSF' ) ) {
  // Set a unique slug-like ID
  $prefix = 'wpvn_ultimate_flatsome';
	
  // Create options
  CSF::createOptions( $prefix, array(
    // framework title
    'framework_title'         => 'Ultimate Flatsome Setting <small>by WPVN Support Team</small>',
    'framework_class'         => $prefix,
    // menu settings
    'menu_title'              => 'UFS Settings',
    'menu_slug'               => 'ultimate-flatsome',
    'menu_type'               => 'menu',
    'menu_capability'         => 'manage_options',
    'menu_icon'               => null,
    'menu_position'           => 2,
    'menu_hidden'             => false,
    'menu_parent'             => '',
    // menu extras
    'show_bar_menu'           => true,
    'show_sub_menu'           => true,
    'show_in_network'         => false,
    'show_in_customizer'      => false,

    'show_search'             => true,
    'show_reset_all'          => true,
    'show_reset_section'      => true,
    'show_footer'             => true,
    'show_all_options'        => true,
    'show_form_warning'       => true,
    'sticky_header'           => false,
    'save_defaults'           => true,
    'ajax_save'               => true,

    // admin bar menu settings
    'admin_bar_menu_icon'     => '',
    'admin_bar_menu_priority' => 99,

    // footer
    'footer_text'             => 'From WPVN Support Team with love 💙💚💛',    
    'footer_after'            => '',
    'footer_credit'           => '',

    // database model
    'database'                => '', // options, transient, theme_mod, network
    'transient_time'          => 0,

    // contextual help
    'contextual_help'         => array(),
    'contextual_help_sidebar' => '',

    // typography options
    'enqueue_webfont'         => true,
    'async_webfont'           => false,

    // others
    'output_css'              => true,

    // theme and wrapper classname
    'nav'                     => 'normal',
    'theme'                   => 'light',
    'class'                   => '',

    // external default values
    'defaults'                => array(),
  ) );


  // Create a section
  CSF::createSection( $prefix, array(
    'title'  => 'Tổng quan',
    'fields' => array(
     
    )
  ) );

    // Create a section
  CSF::createSection( $prefix, array(
    'title'  => 'Flatsome Helper',
    'fields' => array(
      array(
        'type'    => 'heading',
        'content' => 'Bookmark truy cập nhanh một số tính năng',
      ),
      array(
        'type'    => 'content',
        'content' => '<b>Đổi logo:</b> <a href="/wp-admin/customize.php?autofocus%5Bsection%5D=title_tagline" target=_blank> Truy cập Admin dashboard -> Flatsome -> Advanced -> Global Settings</a>',
      ),
      array(
        'type'    => 'content',
        'content' => '<b>Edit nội dung trang chủ:</b> <a href="/wp-admin/post.php?post='.get_option('page_on_front').'&action=edit&app=uxbuilder&type=editor" target=_blank> Truy cập Admin dashboard -> Trang -> Tất cả các trang -> Trang chủ -> Edit with UXBuilder</a>',
      ),
      array(
        'type'    => 'content',
        'content' => '<b>Sửa Nội dung trang</b> <a href="/wp-admin/admin.php?page=optionsframework&tab=of-option-globalsettings" target=_blank> Truy cập Admin dashboard -> Flatsome -> Advanced -> Global Settings</a> để quản lý gắn mã!',
      ),
      array(
        'type'    => 'content',
        'content' => '<b>Sửa Nội dung trang</b> <a href="/wp-admin/admin.php?page=optionsframework&tab=of-option-globalsettings" target=_blank> Truy cập Admin dassboard -> Flatsome -> Advanced -> Global Settings</a> để quản lý gắn mã!',
      ),
      array(
        'type'    => 'content',
        'content' => '<b>Sửa Nội dung trang</b> <a href="/wp-admin/admin.php?page=optionsframework&tab=of-option-globalsettings" target=_blank> Truy cập Admin dashboard -> Flatsome -> Advanced -> Global Settings</a> để quản lý gắn mã!',
        
      ),
    )
  ) );
  
  // Create a section
  CSF::createSection( $prefix, array(
    'title'  => 'Tuỳ chỉnh Template',
    'fields' => json_decode(get_option('wpvnuf_list_posttype'),true),
  ) );

  CSF::createSection( $prefix, array(
    'title'  => 'Backup / Import',
    'fields' => array(
      // A textarea field
      array(
        'id'    => 'backup-and-import',
        'type'  => 'backup',
        'title' => 'Sao lưu và khôi phục dữ liệu plugin',
      ),
    )
  ) );
}
</pre>