---
title: Excel では XLL コードへのアクセス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- accessing xll code [excel 2007],XLLs [Excel 2007], accessing code,commands [Excel 2007], registration,functions [Excel 2007], registration,calling XLLs from Excel,registering commands [Excel 2007],registering functions [Excel 2007]
localization_priority: Normal
ms.assetid: 6e4bf1f3-8eca-4be5-9632-75355ac31d61
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 1523f9e8213cb955f1bfd995c42f921b001299fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798768"
---
# <a name="accessing-xll-code-in-excel"></a>Excel では XLL コードへのアクセス

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
XLL �Ɋ܂܂��֐���R�}���h�� Microsoft Excel �ŃA�N�Z�X�ł���悤�ɂ���ɂ́A���̎������K�v�ƂȂ�܂��B
  
- XLL �ɂ���ăG�N�X�|�[�g����Ȃ���΂Ȃ�܂���B
    
- Excel �ɓo�^����K�v������܂��B
    
## <a name="registering-functions-and-commands-with-excel"></a>Excel の関数とコマンドを登録します。

�o�^���邱�Ƃɂ���āADLL �G���g�� �|�C���g�ɂ��Ď��̂��Ƃ� Excel �Ɏw�����܂��B
  
- ��\�����ǂ����B�܂��֐��̏ꍇ�ɂ́A�֐��E�B�U�[�h�ɕ\�����邩�ǂ����B
    
- XLM �}�N���V�[�g����̂݌Ăяo���邩�A���邢�̓��[�N�V�[�g�����Ăяo���邩�B
    
- �R�}���h�̏ꍇ�A���[�N�V�[�g�֐����A�܂��̓}�N���V�[�g�����֐����ǂ����B
    
- XLL/DLL �G�N�X�|�[�g���A����� Excel �Ŏg�p���閼�O�B
    
- �֐��̏ꍇ:
    
  - �Ԃ��f�[�^�^�A����ш����Ƃ��Ď��f�[�^�^�B
    
  - ������C���v���[�X�ŕύX���Č��ʂ�Ԃ����ǂ����B
    
  - ���������ǂ����B
    
  - �X���b�h �Z�[�t�ł��邩�ǂ��� (Excel 2007 �ȍ~�ŃT�|�[�g����Ă��܂�)�B
    
  - �֐��\��t���E�B�U�[�h�ƃI�[�g�R���v���[�g �G�f�B�^�[�ɁA�֐��̌Ăяo����x�����邽�߂ɕ\������e�L�X�g�B
    
  - ���X�g�\���Ɏg�p����֐��J�e�S���B
    
�O�q�̓_�́A���ׂ� C API �֐��� [xlfRegister](xlfregister-form-1.md) ��g�p���čs���܂��B���̊֐��� XLM �֐��� **REGISTER** �ɑ������܂��B
  
## <a name="calling-xll-functions-directly-from-excel"></a>Excel から直接 XLL 関数の呼び出し

XLL ���[�N�V�[�g�֐��ƃ}�N���V�[�g�֐���o�^����ƁA�g�ݍ��݊֐���Ăяo�����Ƃ��\�Ȏ��Ɏ������ׂĂ̏ꏊ���炻����Ăяo���܂��B
  
- ���[�N�V�[�g�̒P��Z���܂��͔z�񐔎��B
    
- �}�N���V�[�g�̒P��Z���܂��͔z�񐔎��B
    
- 定義された名前の定義。
    
- ����t�������̃_�C�A���O �{�b�N�X�́A����Ɛ����̃t�B�[���h�B
    
- C API �֐� [xlUDF](xludf.md) ���đ��̃A�h�C������B
    
- **Application.Run** ���\�b�h���� Visual Basic for Applications (VBA) ����B 
    
C API �֐� **xlfCaller** ��g�p����ƁA�֐���̌Ăяo�����Z���ւ̎Q�Ƃ܂��̓Z���͈̔͂�擾�ł��܂��B�֐����Z���̏���t������������Ăяo���ꂽ�ꍇ�A�֘A���� 1 �܂��͕����̃Z���ւ̎Q�Ƃ�Ԃ��Ă���Ƃ��ɂ́A�Z���̐����� XLL �֐����܂܂�Ă���Ƃ͌���܂���B�֐��� VBA ���[�U�[��`�֐� (UDF) ����Ăяo���ꂽ�ꍇ�A **xlfCaller** �� VBA �֐���Ăяo�����Z���̃A�h���X��ĂѕԂ��܂��B�ڂ����́A�u [xlfCaller](xlfcaller.md)�v��������������B
  
> [!NOTE]
> Excel は、XLL 関数のコードを**貼り付け関数ウィザード**と**置換**] ダイアログ ボックスから呼び出しも行います。 場合は、関数が、実行に長い時間にかかることが特に、**貼り付けの関数の引数**] ダイアログ ボックスのコードの通常の実行を制限する必要があります。 前面のウィンドウは、これらのダイアログ ボックスのいずれかと、その場合は、すべての開いているウィンドウを反復処理するプロジェクトのいくつかのコードを実装する必要がある場合が呼び出される関数がこれらのダイアログ ボックスのいずれかを検出するためにどちらかです。 
  
## <a name="calling-xll-commands-directly-from-excel"></a>XLL コマンドを Excel から直接呼び出すこと

XLL �R�}���h��o�^����ƁA���̃��[�U�[��`�}�N����Ăяo�����Ƃ��ł��鎟�Ɏ�����������@�� XLL �R�}���h��Ăяo�����Ƃ��ł��܂��B
  
- ���[�N�V�[�g�ɖ��ߍ��܂�Ă���R���g���[�� �I�u�W�F�N�g�Ɋ֘A�t���邱�Ƃɂ���āB
    
- [�}�N���̎��s] �_�C�A���O �{�b�N�X����B
    
- **Application.Run** ���\�b�h��g�p���� VBA ���[�U�[��`�}�N������B 
    
- �J�X�^�}�C�Y���ꂽ���j���[���ڂ܂��̓c�[���o�[����B
    
- �R�}���h��o�^����Ƃ��ɃZ�b�g�A�b�v�����V���[�g�J�b�g �L�[�{�[�h�����g�p���āB
    
- �w�肵���C�x���g���g���b�v�����Ƃ��Ɏ��s����R�}���h�Ƃ��āB
    
> [!NOTE]
> XLL コマンドは非表示で、Excel のダイアログ ボックスで使用できるマクロの一覧に表示されません。ただし、[マクロ名] フィールドに手動で入力できます。Excel では、それらのダイアログ ボックスで、DLL エクスポート名ではなく登録されたとおりの名前であることが必要となります。 
  
Excel �ɓo�^����Ă��邷�ׂĂ� XLL �R�}���h�́A���̌`���ł��邱�Ƃ� Excel �őz�肳��Ă��܂��B
  
```cs
short WINAPI xll_cmd_name(void)
{
// Function code...
    return 1;
}

```

Excel �ł́AXLM �}�N���V�[�g����Ăяo���ꂽ�ꍇ������߂�l����������܂��B�}�N���V�[�g����Ăяo���ꂽ�ꍇ�ɂ́A�߂�l�� **TRUE** �܂��� **FALSE** �ɕϊ�����܂��B���̂��߁A�R�}���h������Ɏ��s���ꂽ�ꍇ�ɂ� 1 ��A���s�������A���[�U�[�ɂ���ăL�����Z�����ꂽ�ꍇ�ɂ� 0 ��Ԃ��悤�ɂ��܂��B
  
C API �֐��� **xlfCaller** ��g�p����ƁA�R�}���h���Ăяo���ꂽ���@�ɂ��Ă̏���擾�ł��܂��B�ڂ����́A�u [xlfCaller](xlfcaller.md)�v��������������B
  
Excel 2007 �ȍ~�̃��[�U�[ �C���^�[�t�F�C�X�͈ȑO�̃o�[�W�����̂�̂Ƃ͑傫���قȂ�܂��B�قƂ�ǂ̏ꍇ�A�J�X�^�� ���j���[ �o�[�A���j���[�A�T�u���j���[�A���j���[���ځA���[�U�[�ݒ�c�[���o�[�A�c�[���o�[ �{�^���̒ǉ��ƍ폜��s���� C API �֐������������T�|�[�g����Ă��܂��B�������A�K������A���[�U�[������܂łɊ���Ă�����@�Œǉ����ڂ��g�p�\�ɂȂ�킯�ł͂���܂���B�ǉ��@�\�������������p�ł��邩�ǂ����𒍈ӂ��Ċm�F���A���p�ł��Ȃ��ꍇ�ɂ̓o�[�W�����ŗL�̃J�X�^�}�C�Y��������Ă��������BExcel 2007 �ȍ~�A���[�U�[ �C���^�[�t�F�C�X�̓}�l�[�W �R�[�h ���W���[����g�p���čœK�̕��@�ŃJ�X�^�}�C�Y����Ă��āAXLL �R�}���h�Ɩ��ɘA�������邱�Ƃ��ł��܂��B
  
## <a name="see-also"></a>�֘A����

- [XLL ��쐬����](creating-xlls.md)
- [関数ウィザードまたは [置換] ダイアログ ボックスから XLL 関数の呼び出し](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
- [�A�h�C�� �}�l�[�W���[�� XLL �C���^�[�t�F�C�X�֐�](add-in-manager-and-xll-interface-functions.md)
- [Excel XLL �̊J��](developing-excel-xlls.md)



