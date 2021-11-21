
TextSwitcher
        android:id="@+id/txtSwitcher"
        android:layout_width="match_parent"
        android:layout_height="wrap_content

TextSwitcher switcher = (TextSwitcher)findViewById(txtSwitcher);
    switcher.setFactory(new ViewFactory() {
        @Override
        public View makeView() {
            TextView t = new TextView(ActivityClass.this);
            //do other stuff the suit your needs
            return t;
        }
    });

    Animation in = AnimationUtils.loadAnimation(this,
            android.R.anim.slide_in_left);
    Animation out = AnimationUtils.loadAnimation(this,
            android.R.anim.slide_out_right);

    switcher.setInAnimation(in);
    switcher.setOutAnimation(out);
