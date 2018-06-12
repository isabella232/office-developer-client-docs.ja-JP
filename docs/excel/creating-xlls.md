---
title: XLL ��쐬����
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- dlls [excel 2007], calling into excel,xlAutoFree function [Excel 2007],xlAutoFree12 function [Excel 2007],xlcall32.lib [Excel 2007],xlAutoRegister function [Excel 2007],xlcall.cpp [Excel 2007],xlAutoRemove function [Excel 2007],xlAddInManagerInfo function [Excel 2007],xlAutoAdd function [Excel 2007],xlAutoOpen function [Excel 2007],xlAutoClose function [Excel 2007],DLLs [Excel 2007], turning into XLLs,XLLs [Excel 2007], calling into Excel,xlAutoRegister12 function [Excel 2007],xlcall.h [Excel 2007],xlAddInManagerInfo12 function [Excel 2007]
localization_priority: Normal
ms.assetid: 7754998f-4e13-4a37-9724-43b6ee6c919b
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: de347d34768c25adf0d96642b4fade781ae26a9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798781"
---
# <a name="creating-xlls"></a>XLL ��쐬����

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
DLL は、自己完結型は、またはその他のライブラリにのみ依存しています、その機能とコマンドにアクセスするための Microsoft Excel を有効にする方法を知る必要があります。 詳細については、 [Excel でのアクセスの Dll](how-to-access-dlls-in-excel.md)を参照してください。 
  
�������ADLL �� Excel �̋@�\�ɃA�N�Z�X����K�v������ꍇ (���Ƃ��΁A�Z���̓�e��擾����Ƃ���A���[�N�V�[�g�֐���Ăяo���Ƃ��A�܂��� Excel ��Ɖ�ă��[�N�X�y�[�X����擾����Ƃ��Ȃ�) �́A�R�[�h���� Excel �ւ̃R�[���o�b�N���\�łȂ���΂Ȃ�܂���B
  
Excel C API �ɂ́ADll ���� Excel �ւ̃R�[���o�b�N��\�ɂ��邢�����̋@�\������܂��B�����ɃA�N�Z�X����ɂ́ADLL �� Excel �� 32 �r�b�g�Ń��C�u���� (xlcall32.lib) �ɃR���p�C�����ɐÓI�Ƀ����N������K�v������܂��B���̐ÓI���C�u�����́AMicrosoft Excel 2013 XLL SDK �̈ꕔ�Ƃ��� Microsoft ����_�E�����[�h�\�ł��BXLL SDK �ɂ́A���̃��C�u������ 32 �r�b�g�ł� 64 �r�b�g�ł̗������܂܂�Ă��܂��B
  
## <a name="enabling-dlls-to-call-back-into-excel"></a>Dll ���� Excel �ւ̃R�[���o�b�N��\�ɂ���

DLL �� Excel �̋@�\�ɃA�N�Z�X���ă��[�N�X�y�[�X����擾����ѐݒ�ł���悤�ɂ��邽�߂ɂ́A�܂� Excel �̃R�[���o�b�N�֐� **Excel4**�A **Excel4v**�A **Excel12**�A����� **Excel12v** �̃A�h���X��擾����K�v������܂��B�Ō�� 2 �̊֐��� Excel 2007 �œ������ꂽ��̂ł���A�㑱�̃o�[�W�����Ŏg�p�\�ł��B�����̂��ׂĂɃA�N�Z�X����ɂ́ADLL �v���W�F�N�g�� Excel 2013 XLL SDK �̈ȉ��Ɏ����t�@�C���ւ̎Q�Ƃ�܂߂�K�v������܂��B (�ǂ̃o�[�W������ Excel �ɂ�܂܂��) �ŏ��� 2 �̃R�[���o�b�N�݂̂ɃA�N�Z�X����ꍇ�́A�ŏ��� 2 �̃t�@�C���݂̂�v���W�F�N�g�Ɋ܂߂�K�v������܂��B
  
### <a name="xlcallh"></a>Xlcall.h

Xlcall.h �t�@�C���ɂ́A���̍��ڂ��܂܂�܂��B
  
- ���ׂẴR�[���o�b�N�֐��̊֐��v���g�^�C�v�B
    
- DLL/XLL と ExcelDLL 間でのデータ交換にコールバックが使用するデータ構造の定義、データ型定数の定義。
    
- ���[�N�V�[�g�֐��A�}�N�� �V�[�g�֐��A����уT�|�[�g����Ă��� Excel �R�}���h�ɑ������� C API �֐��ƃR�}���h�̒�`�B
    
- �R�[���o�b�N�֐��̖߂�l�̒�`�B
    
���̃t�@�C���ł́AC API �ɃA�N�Z�X���邷�ׂẴt�@�C���A�܂��� C API ���g�p����f�[�^�^��������邷�ׂẴt�@�C���ɂ����āA���̃t�@�C���� **#include** �f�B���N�e�B�u�� (���ځA���邢�͕ʂ̃w�b�_�[ �t�@�C�����ĊԐړI��) �g�p����K�v������܂��B 
  
### <a name="xlcall32lib"></a>Xlcall32.lib

Xlcall32.lib ���C�u�����́A�ŏ��� 2 �̃R�[���o�b�N **Excel4** ����� **Excel4v** �̑��A **XlCallVer** �֐���G�N�X�|�[�g���܂��B�v���W�F�N�g�ɂ��̃��C�u�����ւ̎Q�Ƃ��Ȃ��ƁA�R�[�h��ł����̃R�[���o�b�N�̂����ꂩ��g�p���Ă���ꍇ�A�����J�[�� XLL ��쐬�ł��܂���B(�����̊֐��̃A�h���X�́A�ʏ�� Excel �̃C���X�g�[���̈�Ƃ��ăV�X�e���ɃR�s�[����铯���� Xlcall32.dll �ɓ��I�Ƀ����N���邱�ƂŎ擾�ł��܂��B) 
  
### <a name="xlcallcpp"></a>Xlcall.cpp

Excel �R�[���o�b�N **Excel12** ����� **Excel12v** �� Xlcall32.lib �ł̓G�N�X�|�[�g����܂���B����ɂ��AExcel 2007 �ȍ~�ō쐬���� XLL �v���W�F�N�g��������O�̃o�[�W������ Excel �ł����ł���悤�ɂȂ��Ă��܂��BXlcall.cpp ���W���[���ɂ́A **Excel12** �֐��� **Excel12v** �֐��̃R�[�h���܂܂�Ă��܂��B�����́AExcel 2007 �ȍ~�ł� Excel �̃G���g�� �|�C���g��Ăяo���A������O�̃o�[�W������ Excel ����s���Ă���ꍇ�͈��S�ȃG���[�l��Ԃ��܂��BExcel 2007 �ȍ~�œ��삵�A��K�͂ȃO���b�h�ƒ��� Unicode ��������������V�����f�[�^�^��g�p�ł��� XLL ��쐬����ꍇ�́A�v���W�F�N�g�ɂ��̃��W���[����܂߂�K�v������܂��B 
  
> [!NOTE]
> [!����] Excel 2010 SDK �ȍ~�ł́A���̃t�@�C���� 32 �r�b�g�� 64 �r�b�g�̗����� XLL �ɃR���p�C���ł��܂��B 
  
## <a name="turning-dlls-into-xlls-add-in-manager-interface-functions"></a>DLL �� XLL �ɂ���:�A�h�C�� �}�l�[�W���[ �C���^�[�t�F�C�X�֐�

XLL は、Excel または Excel のアドイン マネージャーによって呼び出されるいくつかの手順をエクスポートする DLL です。 これらの手順はここで簡単に説明し、[アドイン マネージャーおよび XLL インターフェイスの関数](add-in-manager-and-xll-interface-functions.md)で詳しく説明します。 **XlAuto**のプレフィックスを持つすべてのこれらの DLL のコールバックを起動します。 これらのコマンドの**xlAutoOpen**では、1 つだけです。 アドインをアクティブ化し、XLL 関数を登録するのには通常使用してコマンドを excel やその他の初期化タスクを実行するときに呼び出されます。 後のセクションでは、関数のシグネチャとのすべての**xlAuto**関数の実装の例が用意されています。 
  
�����̃R�[���o�b�N�̒��ŕK�{�Ȃ̂� **xlAutoOpen** �����ł����A�A�h�C���̓���ɂ���ẮA���̃R�}���h��G�N�X�|�[�g����K�v������\��������܂��B 
  
Excel 2007 �ł́A��K�͂ȃO���b�h�ւ̑Ή��ƒ��� Unicode ������̃T�|�[�g�̂��߂ɁA�V�����f�[�^�^ **XLOPER12** ����������܂����B **XLOPER12** �ɂ��ẮA���̃g�s�b�N�Ō�ɐ�����܂��B **xlAuto** �֐��͌Â��f�[�^�^�ł��� **XLOPER** ��󂯎������Ԃ����肷��̂ɑ΂��AExcel 2007 �œ������ꂽ���̊֐��̐V�����o�[�W������ **XLOPER12** �f�[�^�^��g�p���܂��B **XLOPER12** ������ ���[�N������邽�߂Ɏ������K�{�ł��邱�Ƃ����� **xlAutoFree12** ��ʂɂ���΁A���ׂẴo�[�W���� 12 �� **xlAuto** �֐��͏ȗ����Ă���S��̖��͂���܂���B�ȗ�����ꍇ�AExcel 2007 �ȍ~�� Excel �� **XLOPER** �o�[�W������Ăяo���܂��B 
  
### <a name="xlautoopen"></a>xlAutoOpen

XLL ���A�N�e�B�u�������ƁAExcel �� [xlAutoOpen](xlautoopen.md) �֐���Ăяo���܂��BExcel �Z�b�V�������J�n����Ƃ��ɂ́A����I�������O��� Excel �Z�b�V�����ŃA�N�e�B�u�ł������A�h�C�����A�N�e�B�u������܂��B�A�h�C���́AExcel �Z�b�V�������ɓǂݍ��܂��ƁA�A�N�e�B�u�ɂȂ�܂��B�A�h�C���́AExcel �Z�b�V�������ɔ�A�N�e�B�u��������A�ăA�N�e�B�u�������肷�邱�Ƃ��ł��܂��B�ăA�N�e�B�u������ۂɂ͊֐����Ăяo����܂��B 
  
XLL �̊֐��ƃR�}���h�̓o�^�A�f�[�^�\���̏������A���[�U�[ �C���^�[�t�F�C�X�̃J�X�^�}�C�Y�Ȃǂ�s���ɂ́A **xlAutoOpen** ��g�p����K�v������܂��B 
  
�A�h�C���� [xlAutoRegister](xlautoregister-xlautoregister12.md) �֐��� [xlAutoRegister12](xlautoregister-xlautoregister12.md) �֐����������уG�N�X�|�[�g����ꍇ�AExcel ����� **xlAutoOpen** �֐���Ăяo�����Ɋ֐���R�}���h��A�N�e�B�u�ɂ��ēo�^���悤�Ƃ��邱�Ƃ�����܂��B���̏ꍇ�́A�֐��܂��̓R�}���h���������@�\����悤�ɁA�A�h�C�����\���ɏ���������Ă��邱�Ƃ�m�F����K�v������܂��B�����Ȃ��Ă��Ȃ��ꍇ�A�֐���R�}���h�̓o�^��A�K�v�ȏ������̎��s�����s���܂��B 
  
### <a name="xlautoclose"></a>xlAutoClose

XLL ����A�N�e�B�u�������ƁAExcel �� [xlAutoClose](xlautoclose.md) �֐���Ăяo���܂��BExcel �Z�b�V����������ɏI������ƁA�A�h�C���͔�A�N�e�B�u������܂��BExcel �Z�b�V�������Ƀ��[�U�[���A�h�C�����A�N�e�B�u������ƁA�֐����Ăяo����܂��B 
  
�֐��ƃR�}���h�̓o�^����A���\�[�X�̉���A�J�X�^�}�C�Y�̉���Ȃǂ�s���ɂ́A **xlAutoClose** ��g�p����K�v������܂��B 
  
> [!NOTE]
> [!����] �֐��ƃR�}���h�̓o�^����Ɋւ��ẮA���m�̖�肪����܂��B�ڂ����́A�u[Excel �A�h�C�� (XLL) �J���ɂ�������m�̖��](known-issues-in-excel-xll-development.md)�v��������������B 
  
### <a name="xlautoadd"></a>xlAutoAdd

Excel は、ユーザーは、アドイン マネージャーを使用して Excel セッション中に、XLL を起動するたびに、 [xlAutoAdd 関数](xlautoadd.md)を呼び出します。 Excel が起動し、インストール済みのアドインをロードするとき、この関数は呼び出されません。 
  
���̊֐���g�p���āA�A�h�C�����A�N�e�B�u�ɂȂ��Ă��邱�Ƃ���[�U�[�ɒʒm����J�X�^�� �_�C�A���O �{�b�N�X�̕\���A���W�X�g���ɑ΂���ǂݏ����A�܂��̓��C�Z���X���̊m�F��s�����Ƃ��ł��܂��B
  
### <a name="xlautoremove"></a>xlAutoRemove

Excel は、ユーザーが非アクティブ化、XLL Excel セッション中にアドイン マネージャーを使用してたびに、 [xlAutoRemove](xlautoremove.md)関数を呼び出します。 Excel のセッションを終了すると、正常または異常では、アドインがインストールされていると、この関数は呼び出されません。 
  
���̊֐���g�p���āA�A�h�C������A�N�e�B�u�ɂȂ��Ă��邱�Ƃ���[�U�[�ɒʒm����J�X�^�� �_�C�A���O �{�b�N�X��\��������A���W�X�g���ւ̓ǂݏ�����s�����Ƃ��ł��܂��B
  
### <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a>xlAddInManagerInfo/xlAddInManagerInfo12

�A�h�C�� �}�l�[�W���[�� Excel �Z�b�V�����ŏ��߂ČĂяo�����Ƃ��AExcel �� [xlAddInManagerInfo](xladdinmanagerinfo-xladdinmanagerinfo12.md) �֐���Ăяo���܂��BExcel �� 1 �Ɠ�����������n���ꍇ�A���̊֐��͕����� (�ʏ�́A�A�h�C���̖��O) ��Ԃ��K�v������܂��B����ȊO�̏ꍇ�́A **#VALUE!** ��Ԃ��K�v������܂��B
  
Excel 2007 �ȍ~�ł́A **xlAddInManagerInfo12** �֐��� XLL �ɂ���ăG�N�X�|�[�g����Ă���ꍇ�AExcel �͂��̊֐��� **xlAddInManagerInfo** �֐�����D�悵�ČĂяo���܂��B�o�[�W�����ɂ���� XLL �̓���ɈႢ�������邱�Ƃ����邽�߂ɁA **xlAddInManagerInfo12** �֐��� **xlAddInManagerInfo** �֐��͓�����������K�v������܂��B **xlAddInManagerInfo12** �֐��� **XLOPER12** �f�[�^�^��Ԃ��K�v������A **xlAddInManagerInfo** �֐��� **XLOPER** �f�[�^�^��Ԃ��K�v������܂��B 
  
### <a name="xlautoregisterxlautoregister12"></a>xlAutoRegister/xlAutoRegister12

XLM �֐� [REGISTER](xlautoregister-xlautoregister12.md) �܂��͂���Ɠ����� C API �֐� **xlfRegister** ���Ăяo���ꂽ�Ƃ��A�o�^�Ώۂ̊֐��̖߂�l�ƈ����̌^���w�肳��Ă��Ȃ��ƁAExcel �� [xlAutoRegister](xlfregister-form-1.md) �֐���Ăяo���܂��B **xlAutoRegister** �֐��ɂ��AXLL �͂��̓���ɂ���G�N�X�|�[�g���ꂽ�֐��ƃR�}���h�̃��X�g��������Ă��̊֐�������ƂƂ�ɓo�^���A�w�肳�ꂽ�^��Ԃ����Ƃ��ł��܂��B 
  
Excel 2007 �ȍ~�ł́A **xlAddInRegister12** �֐��� XLL �ɂ���ăG�N�X�|�[�g����Ă���ꍇ�AExcel �͂��̊֐��� **xlAddInRegister** �֐�����D�悵�ČĂяo���܂��B 
  
> [!NOTE]
> [!����] �����Ɩ߂�l�̌^�̎w�肪�Ȃ��܂܂� **xlAddInRegister**/  **xlAddInRegister12** ���֐���o�^���悤�Ƃ���΁A�ċA�I�ȌĂяo���̃��[�v���������A�ŏI�I�ɂ̓R�[�� �X�^�b�N���I�[�o�[�t���[���� Excel ���I�����邩�A�������Ȃ��Ȃ�܂��B 
  
### <a name="xlautofreexlautofree12"></a>xlAutoFree/xlAutoFree12

Excel は XLL ワークシート関数は、 **XLOPER**を取得した後だけに[xlAutoFree と xlAutoFree12](xlautofree-xlautofree12.md)関数を呼び出す/ **XLOPER12**のデータ型、メモリを解放する必要がある、xll ファイルを Excel に指示するフラグを設定します。 これにより、配列、文字列、およびメモリ リークが発生せず、ワークシートへの外部参照を動的に割り当てられている xll ファイルに戻ります。 Excel 2007 以降では、 **XLOPER12**のデータ型はサポートされています。 �ڍׂɂ��ẮA�u[Excel �̃������Ǘ�](memory-management-in-excel.md)�v��Q�Ƃ��Ă��������B
  
> [!NOTE]
> Excel 2007 以降では、Excel が設定されている場合にマルチ スレッドのワークシートの再計算、 **xlAutoFree**を使用して、/ に返される関数を呼び出すだけで使用されていたのと同じスレッドで**xlAutoFree12**関数が呼び出されます。 **XlAutoFree**を/ 、その後のワークシートのセルは、そのスレッドで評価する前に、**xlAutoFree12**が常に行われます。 これには、XLL でスレッド セーフでないデザインが簡素化されます。 詳細については、 [Excel で再計算をマルチ スレッド](multithreaded-recalculation-in-excel.md)を参照してください。 
  
### <a name="creating-64-bit-xlls"></a>64 �r�b�g XLL �̍쐬

Excel ����у��[�U�[��`�֐��́A32 �r�b�g �I�y���[�e�B���O �V�X�e������D�ꂽ�p�t�H�[�}���X����҂ł��� 64 �r�b�g �I�y���[�e�B���O �V�X�e���Ŏ��s�\�ł��BExcel �́A�f�[�^�̌^�Ɋւ������܂� **XLOPER12** �\���̒l��n���܂��B **XLOPER12** �\���ƃl�C�e�B�u�^ ( **int** �܂��͂��傫���^�ɒl��ێ�����|�C���^�[�Ȃ�) �̊ԂŒl��ϊ�����ꍇ�͂����ӂ��������B 
  
## <a name="see-also"></a>�֘A����



[関数ウィザードまたは [置換] ダイアログ ボックスから XLL 関数の呼び出し](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
[�A�h�C�� �}�l�[�W���[�� XLL �C���^�[�t�F�C�X�֐�](add-in-manager-and-xll-interface-functions.md)
  
[Excel XLL �̊J��](developing-excel-xlls.md)

