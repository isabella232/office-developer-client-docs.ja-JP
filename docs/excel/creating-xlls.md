---
title: XLL を作成する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- dlls [excel 2007], calling into excel,xlAutoFree function [Excel 2007],xlAutoFree12 function [Excel 2007],xlcall32.lib [Excel 2007],xlAutoRegister function [Excel 2007],xlcall.cpp [Excel 2007],xlAutoRemove function [Excel 2007],xlAddInManagerInfo function [Excel 2007],xlAutoAdd function [Excel 2007],xlAutoOpen function [Excel 2007],xlAutoClose function [Excel 2007],DLLs [Excel 2007], turning into XLLs,XLLs [Excel 2007], calling into Excel,xlAutoRegister12 function [Excel 2007],xlcall.h [Excel 2007],xlAddInManagerInfo12 function [Excel 2007]
ms.assetid: 7754998f-4e13-4a37-9724-43b6ee6c919b
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 886b8e74f00f2e724785d43475ee0ffa3c922710
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706745"
---
# <a name="creating-xlls"></a>XLL を作成する

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
DLL が自己完結型であるか、他のライブラリのみに依存する場合、Microsoft Excel を有効にしてその関数とコマンドにアクセスする方法について把握しておく必要があります。 詳細については、「[Excel で DLL にアクセスする](how-to-access-dlls-in-excel.md)」を参照してください。 
  
ただし、DLL が Excel の機能にアクセスする必要がある場合 (たとえば、セルの内容を取得するときや、ワークシート関数を呼び出すとき、または Excel を照会してワークスペース情報を取得するときなど) は、コードから Excel へのコールバックが可能でなければなりません。
  
Excel C API �ɂ́ADll ���� Excel �ւ̃R�[���o�b�N��\�ɂ��邢�����̋@�\������܂��B�����ɃA�N�Z�X����ɂ́ADLL �� Excel �� 32 �r�b�g�Ń��C�u���� (xlcall32.lib) �ɃR���p�C�����ɐÓI�Ƀ����N������K�v������܂��B���̐ÓI���C�u�����́AMicrosoft Excel 2013 XLL SDK �̈ꕔ�Ƃ��� Microsoft ����_�E�����[�h�\�ł��BXLL SDK �ɂ́A���̃��C�u������ 32 �r�b�g�ł� 64 �r�b�g�ł̗������܂܂�Ă��܂��B
  
## <a name="enabling-dlls-to-call-back-into-excel"></a>Dll から Excel へのコールバックを可能にする

DLL �� Excel �̋@�\�ɃA�N�Z�X���ă��[�N�X�y�[�X����擾����ѐݒ�ł���悤�ɂ��邽�߂ɂ́A�܂� Excel �̃R�[���o�b�N�� **Excel4**�A **Excel4v**�A **Excel12**�A����� **Excel12v** �̃A�h���X��擾����K�v������܂��B�Ō�� 2 �̊��� Excel 2007 �œ������ꂽ��̂ł���A�㑱�̃o�[�W�����Ŏg�p�\�ł��B�����̂��ׂĂɃA�N�Z�X����ɂ́ADLL �v���W�F�N�g�� Excel 2013 XLL SDK �̈ȉ��Ɏ����t�@�C���ւ̎Q�Ƃ�܂߂�K�v������܂��B (�ǂ̃o�[�W������ Excel �ɂ�܂܂��) �ŏ��� 2 �̃R�[���o�b�N�݂̂ɃA�N�Z�X����ꍇ�́A�ŏ��� 2 �̃t�@�C���݂̂�v���W�F�N�g�Ɋ܂߂�K�v������܂��B
  
### <a name="xlcallh"></a>Xlcall.h

Xlcall.h ファイルには、次の項目が含まれます。
  
- すべてのコールバック関数の関数プロトタイプ。
    
- DLL/XLL と ExcelDLL 間でのデータ交換にコールバックが使用するデータ構造の定義、データ型定数の定義。
    
- ワークシート関数、マクロ シート関数、およびサポートされている Excel コマンドに相当する C API 関数とコマンドの定義。
    
- コールバック関数の戻り値の定義。
    
���̃t�@�C���ł́AC API �ɃA�N�Z�X���邷�ׂẴt�@�C���A�܂��� C API ���g�p����f�[�^�^��������邷�ׂẴt�@�C���ɂ����āA���̃t�@�C���� **#include** �f�B���N�e�B�u�� (���ځA���邢�͕ʂ̃w�b�_�[ �t�@�C�����ĊԐړI��) �g�p����K�v������܂��B 
  
### <a name="xlcall32lib"></a>Xlcall32.lib

Xlcall32.lib ���C�u�����́A�ŏ��� 2 �̃R�[���o�b�N **Excel4** ����� **Excel4v** �̑��A **XlCallVer** ����G�N�X�|�[�g���܂��B�v���W�F�N�g�ɂ��̃��C�u�����ւ̎Q�Ƃ��Ȃ��ƁA�R�[�h��ł����̃R�[���o�b�N�̂����ꂩ��g�p���Ă���ꍇ�A�����J�[�� XLL ��쐬�ł��܂���B(�����̊��̃A�h���X�́A�ʏ�� Excel �̃C���X�g�[���̈�Ƃ��ăV�X�e���ɃR�s�[����铯���� Xlcall32.dll �ɓ��I�Ƀ����N���邱�ƂŎ擾�ł��܂��B) 
  
### <a name="xlcallcpp"></a>Xlcall.cpp

Excel �R�[���o�b�N **Excel12** ����� **Excel12v** �� Xlcall32.lib �ł̓G�N�X�|�[�g����܂���B����ɂ��AExcel 2007 �ȍ~�ō쐬���� XLL �v���W�F�N�g��������O�̃o�[�W������ Excel �ł����ł���悤�ɂȂ��Ă��܂��BXlcall.cpp ���W���[���ɂ́A **Excel12** ���� **Excel12v** ���̃R�[�h���܂܂�Ă��܂��B�����́AExcel 2007 �ȍ~�ł� Excel �̃G���g�� �|�C���g��Ăяo���A������O�̃o�[�W������ Excel ����s���Ă���ꍇ�͈��S�ȃG���[�l��Ԃ��܂��BExcel 2007 �ȍ~�œ��삵�A��K�͂ȃO���b�h�ƒ��� Unicode ��������������V�����f�[�^�^��g�p�ł��� XLL ��쐬����ꍇ�́A�v���W�F�N�g�ɂ��̃��W���[����܂߂�K�v������܂��B 
  
> [!NOTE]
> Excel 2010 SDK 以降では、このファイルは 32 ビットと 64 ビットの両方の XLL にコンパイルできます。 
  
## <a name="turning-dlls-into-xlls-add-in-manager-interface-functions"></a>DLL �� XLL �ɂ���:�A�h�C�� �}�l�[�W���[ �C���^�[�t�F�C�X��

XLL は、Excel または Excel のアドイン マネージャーによって呼び出されるいくつかのプロシージャをエクスポートする DLL です。ここでは、これらのプロシージャを簡単に説明します。詳細な説明については、「[アドイン マネージャーと XLL インターフェイス関数](add-in-manager-and-xll-interface-functions.md)」を参照してください。これらの DLL コールバックはすべてプレフィックス **xlAuto** で始まります。これらのうち必須コマンドは **xlAutoOpen** のみです。これは、アドインが有効になると呼び出され、通常は Excel に XLL の関数とコマンドを登録してその他の初期化タスクを実行するために使用されます。すべての **xlAuto** 関数の関数シグネチャと実装例は、後のセクションで説明します。  
  
�����̃R�[���o�b�N�̒��ŕK�{�Ȃ̂� **xlAutoOpen** �����ł����A�A�h�C���̓���ɂ���ẮA���̃R�}���h��G�N�X�|�[�g����K�v������\��������܂��B 
  
Excel 2007 �ł́A��K�͂ȃO���b�h�ւ̑Ή��ƒ��� Unicode ������̃T�|�[�g�̂��߂ɁA�V�����f�[�^�^ **XLOPER12** ����������܂����B **XLOPER12** �ɂ��ẮA���̃g�s�b�N�Ō�ɐ�����܂��B **xlAuto** ���͌Â��f�[�^�^�ł��� **XLOPER** ��󂯎������Ԃ����肷��̂ɑ��AExcel 2007 �œ������ꂽ���̊��̐V�����o�[�W������ **XLOPER12** �f�[�^�^��g�p���܂��B **XLOPER12** ������ ���[�N������邽�߂Ɏ������K�{�ł��邱�Ƃ����� **xlAutoFree12** ��ʂɂ���A���ׂẴo�[�W���� 12 �� **xlAuto** ���͏ȗ����Ă���S��̖��͂���܂���B�ȗ�����ꍇ�AExcel 2007 �ȍ~�� Excel �� **XLOPER** �o�[�W������Ăяo���܂��B 
  
### <a name="xlautoopen"></a>xlAutoOpen

XLL ���A�N�e�B�u�������ƁAExcel �� [xlAutoOpen](xlautoopen.md) ����Ăяo���܂��BExcel �Z�b�V�������J�n����Ƃ��ɂ́A����I�������O��� Excel �Z�b�V�����ŃA�N�e�B�u�ł������A�h�C�����A�N�e�B�u������܂��B�A�h�C���́AExcel �Z�b�V�������ɓǂݍ��܂��ƁA�A�N�e�B�u�ɂȂ�܂��B�A�h�C���́AExcel �Z�b�V�������ɔ�A�N�e�B�u��������A�ăA�N�e�B�u�������肷�邱�Ƃ��ł��܂��B�ăA�N�e�B�u������ۂɂ͊����Ăяo����܂��B 
  
XLL �̊��ƃR�}���h�̓o�^�A�f�[�^�\���̏������A���[�U�[ �C���^�[�t�F�C�X�̃J�X�^�}�C�Y�Ȃǂ�s���ɂ́A **xlAutoOpen** ��g�p����K�v������܂��B 
  
�A�h�C���� [xlAutoRegister](xlautoregister-xlautoregister12.md) ���� [xlAutoRegister12](xlautoregister-xlautoregister12.md) �����������уG�N�X�|�[�g����ꍇ�AExcel ����� **xlAutoOpen** ����Ăяo�����Ɋ���R�}���h��A�N�e�B�u�ɂ��ēo�^���悤�Ƃ��邱�Ƃ�����܂��B���̏ꍇ�́A���܂��̓R�}���h���������@�\����悤�ɁA�A�h�C�����\���ɏ���������Ă��邱�Ƃ�m�F����K�v������܂��B�����Ȃ��Ă��Ȃ��ꍇ�A����R�}���h�̓o�^��A�K�v�ȏ������̎��s�����s���܂��B 
  
### <a name="xlautoclose"></a>xlAutoClose

XLL ����A�N�e�B�u�������ƁAExcel �� [xlAutoClose](xlautoclose.md) ����Ăяo���܂��BExcel �Z�b�V����������ɏI������ƁA�A�h�C���͔�A�N�e�B�u������܂��BExcel �Z�b�V�������Ƀ��[�U�[���A�h�C�����A�N�e�B�u������ƁA�����Ăяo����܂��B 
  
���ƃR�}���h�̓o�^����A���\�[�X�̉���A�J�X�^�}�C�Y�̉���Ȃǂ�s���ɂ́A **xlAutoClose** ��g�p����K�v������܂��B 
  
> [!NOTE]
> [!����] ���ƃR�}���h�̓o�^����Ɋւ��ẮA���m�̖�肪����܂��B�ڂ����́A�u[Excel �A�h�C�� (XLL) �J���ɂ�������m�̖��](known-issues-in-excel-xll-development.md)�v��������������B 
  
### <a name="xlautoadd"></a>xlAutoAdd

ユーザーが Excel セッション中にアドイン マネージャーを使用して XLL をアクティブ化すると、Excel は [xlAutoAdd 関数](xlautoadd.md)を呼び出します。Excel が起動して、あらかじめインストールされたアドインを読み込む際には、この関数は呼び出されません。 
  
この関数を使用して、アドインがアクティブになっていることをユーザーに通知するカスタム ダイアログ ボックスの表示、レジストリに対する読み書き、またはライセンス情報の確認を行うことができます。
  
### <a name="xlautoremove"></a>xlAutoRemove

ユーザーが Excel セッション中にアドイン マネージャーを使用して XLL を非アクティブ化すると、Excel は [xlAutoRemove](xlautoremove.md) 関数を呼び出します。アドインがインストールされている状態で Excel セッションが終了するときには、正常終了でも異常終了でも、この関数は呼び出されません。 
  
この関数を使用して、アドインが非アクティブになっていることをユーザーに通知するカスタム ダイアログ ボックスを表示したり、レジストリへの読み書きを行うことができます。
  
### <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a>xlAddInManagerInfo/xlAddInManagerInfo12

�A�h�C�� �}�l�[�W���[�� Excel �Z�b�V�����ŏ��߂ČĂяo�����Ƃ��AExcel �� [xlAddInManagerInfo](xladdinmanagerinfo-xladdinmanagerinfo12.md) ����Ăяo���܂��BExcel �� 1 �Ɠ�����������n���ꍇ�A���̊��͕����� (�ʏ�́A�A�h�C���̖��O) ��Ԃ��K�v������܂��B����ȊO�̏ꍇ�́A **#VALUE!** ��Ԃ��K�v������܂��B
  
Excel 2007 �ȍ~�ł́A **xlAddInManagerInfo12** ���� XLL �ɂ���ăG�N�X�|�[�g����Ă���ꍇ�AExcel �͂��̊��� **xlAddInManagerInfo** ������D�悵�ČĂяo���܂��B�o�[�W�����ɂ���� XLL �̓���ɈႢ�������邱�Ƃ����邽�߂ɁA **xlAddInManagerInfo12** ���� **xlAddInManagerInfo** ���͓�����������K�v������܂��B **xlAddInManagerInfo12** ���� **XLOPER12** �f�[�^�^��Ԃ��K�v������A **xlAddInManagerInfo** ���� **XLOPER** �f�[�^�^��Ԃ��K�v������܂��B 
  
### <a name="xlautoregisterxlautoregister12"></a>xlAutoRegister/xlAutoRegister12

XLM �� [REGISTER](xlautoregister-xlautoregister12.md) �܂��͂���Ɠ����� C API �� **xlfRegister** ���Ăяo���ꂽ�Ƃ��A�o�^�Ώۂ̊��̖߂�l�ƈ����̌^���w�肳��Ă��Ȃ��ƁAExcel �� [xlAutoRegister](xlfregister-form-1.md) ����Ăяo���܂��B **xlAutoRegister** ���ɂ��AXLL �͂��̓���ɂ���G�N�X�|�[�g���ꂽ���ƃR�}���h�̃��X�g��������Ă��̊�������ƂƂ�ɓo�^���A�w�肳�ꂽ�^��Ԃ����Ƃ��ł��܂��B 
  
Excel 2007 �ȍ~�ł́A **xlAddInRegister12** ���� XLL �ɂ���ăG�N�X�|�[�g����Ă���ꍇ�AExcel �͂��̊��� **xlAddInRegister** ������D�悵�ČĂяo���܂��B 
  
> [!NOTE]
> [!����] �����Ɩ߂�l�̌^�̎w�肪�Ȃ��܂܂� **xlAddInRegister**/  **xlAddInRegister12** ������o�^���悤�Ƃ���A�ċA�I�ȌĂяo���̃��[�v���������A�ŏI�I�ɂ̓R�[�� �X�^�b�N���I�[�o�[�t���[���� Excel ���I�����邩�A�������Ȃ��Ȃ�܂��B 
  
### <a name="xlautofreexlautofree12"></a>xlAutoFree/xlAutoFree12

XLL が開放する必要があるメモリがまだあることを Excel に通知するフラグが設定された **XLOPER**/ **XLOPER12** データ型が XLL ワークシート関数から返されると、Excel は [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md) 関数を呼び出します。 これにより、動的に割り当てられた配列、文字列および外部参照をメモリ リークなしに XLL でワークシートに返せるようになります。 **XLOPER12** データ型は、Excel 2007 以降でサポートされています。 詳細については、「[Excel でのメモリ管理](memory-management-in-excel.md)」を参照してください。
  
> [!NOTE]
> Excel 2007 以降では、Excel がマルチ スレッドのワークシートの再計算を使用するように構成されている場合、**xlAutoFree**/ **xlAutoFree12** 関数は、それを返した関数を呼び出すために使用されたスレッドと同じスレッドで呼び出されます。 **xlAutoFree**/ **xlAutoFree12** の呼び出しは、常に、そのスレッドで後続のワークシートのセルが評価される前に行われます。 これにより、XLL でのスレッド セーフな設計が簡単になります。 詳細については、「[Excel でのマルチ スレッドの再計算](multithreaded-recalculation-in-excel.md)」をご参照ください。 
  
### <a name="creating-64-bit-xlls"></a>64 ビット XLL の作成

Excel ����у��[�U�[��`���́A32 �r�b�g �I�y���[�e�B���O �V�X�e������D�ꂽ�p�t�H�[�}���X����҂ł��� 64 �r�b�g �I�y���[�e�B���O �V�X�e���Ŏ��s�\�ł��BExcel �́A�f�[�^�̌^�Ɋւ������܂� **XLOPER12** �\���̒l��n���܂��B **XLOPER12** �\���ƃl�C�e�B�u�^ ( **int** �܂��͂��傫���^�ɒl��ێ�����|�C���^�[�Ȃ�) �̊ԂŒl��ϊ�����ꍇ�͂����ӂ��������B 
  
## <a name="see-also"></a>関連項目



[関数ウィザードまたは [置換] ダイアログ ボックスから XLL 関数を呼び出す](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
[アドイン マネージャーと XLL インターフェイス関数](add-in-manager-and-xll-interface-functions.md)
  
[Excel XLL の開発](developing-excel-xlls.md)

