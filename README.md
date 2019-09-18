# CFGScanDroid_modified
more information outputs of CFG generator tools

the output format of original version:

Lorg/jetbrains/uast/InternalUastUtilsKt.<clinit>()V;3;0:1,2;1:2
Lorg/jetbrains/uast/InternalUastUtilsKt.renderModifiers()Ljava/lang/String;11;0:5;1:6,7;2:3,4;3:5;4:3;5:1,2;6:8,9;7:6;8:10;9:10
Lorg/jetbrains/uast/InternalUastUtilsKt.unwrapParenthesis()Lorg/jetbrains/uast/UExpression;3;0:1,2;2:0
Lorg/jetbrains/uast/UAnnotated$DefaultImpls.findAnnotation()Lorg/jetbrains/uast/UAnnotation;6;0:3;1:5;2:3,4;3:1,2;4:5
Lorg/jetbrains/uast/UAnnotation$DefaultImpls.accept()V;3;0:1,2;1:2
Lorg/jetbrains/uast/UAnnotation$DefaultImpls.asLogString()Ljava/lang/String;7;0:1,2;1:5;2:5;3:6;4:6;5:3,4
Lorg/jetbrains/uast/UAnnotation$DefaultImpls.asRenderString()Ljava/lang/String;6;0:1,2;1:5;2:5;

the output format of new_version:
Lpl/droidsonroids/gif/GifImageView.onRestoreInstanceState()V;3;0(2-IF_NEZ):1(2-IF_NEZ),2(13-null)
Lpl/droidsonroids/gif/GifImageView.onSaveInstanceState()Landroid/os/Parcelable;6;0(3-IF_EQZ):1(3-IF_EQZ),2(2-GOTO);1(2-GOTO):5(3-IF_EQZ);2(2-MOVE_RESULT_OBJECT):5(3-IF_EQZ);4(2-MOVE_RESULT_OBJECT):3(3-IF_EQZ);5(2-IF_EQZ):3(3-IF_EQZ),4(2-GOTO)
Lpl/droidsonroids/gif/GifImageView.setBackgroundResource()V;3;0(4-IF_NEZ):1(4-IF_NEZ),2(1-null);2(1-INVOKE_SUPER):1(4-IF_NEZ)
Lpl/droidsonroids/gif/GifImageView.setImageResource()V;3;0(4-IF_NEZ):1(4-IF_NEZ),2(1-null);2(1-INVOKE_SUPER):1(4-IF_NEZ)
Lpl/droidsonroids/gif/GifImageView.setImageURI()V;9;0(2-IF_EQZ):1(2-IF_EQZ),2(1-CONST_4);1(1-CONST_4):5(2-IF_EQZ);2(12-IF_EQZ):3(2-IF_EQZ),4(1-CONST_4);3(6-GOTO):6(2-IF_EQZ);4(4-INVOKE_DIRECT):6(2-IF_EQZ);5(1-IF_NEZ):7(2-IF_EQZ),8(1-CONST_4);6(5-GOTO):5(2-IF_EQZ);8(1-INVOKE_SUPER):7(2-IF_EQZ)
Lpl/droidsonroids/gif/GifInfoHandle.<clinit>()V;8;0(4-GOTO):1(4-GOTO);2(1-INVOKE_STATIC):1(4-GOTO);3(2-IF_NEZ):4(4-GOTO),5(1-null);4(1-SGET_OBJECT):2(4-GOTO);5(15-GOTO):4(4-GOTO);6(1-IF_NEZ):2(4-GOTO),3(1-null);7(5-THROW):4(4-GOTO)


new version format

startaddress(block_length: destination_operation_code):(destinationAddress(block_length: destination_operation_code)), ...
