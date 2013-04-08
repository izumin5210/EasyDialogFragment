# EasyDialogFragment
DialogFragmentを用いたダイアログを簡単に扱える（？）

## いま使えるDialog
* AlertDialog
* ProgressDialog（STYLE_SPINNERのみ）

## 使い方
### AlertDialogFragment
    public class HogeFragment extends Fragment implements AlertDialogFragment.Callbacks {
        @Override
        public void onActivityCreated(Bundle savedInstanceSate) {
            super.onActivityCreated(savedInstanceSate);
            // いろいろほげほげする

            AlertDialogFragment.Builder builder = new AlertDialogFragment.Builder();
            // いつも通りbuilderにいろいろsetする
            // ...
            // ...
            builder.create().show(getFragmentManger(), "alert_dialog");
        }

        @Override
        public void onDialogClicked(DialogInterface dialog, int whick) {
            // ボタンクリック時の処理
        }

        @Override
        public void onDialogCanceled(DialogInterface dialog) {
            // ダイアログキャンセル時の処理
        }
    }

### ProgressDialogFragment

`ProgressDialogFragment.Builder`から適当に．
