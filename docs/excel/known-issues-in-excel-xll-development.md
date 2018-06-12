---
title: Excel �A�h�C�� (XLL) �J���ɂ�������m�̖��
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- known issues [excel 2007]
localization_priority: Normal
ms.assetid: 3dfecc0b-a91c-448e-8721-5d3486b625fa
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 9cdbb10ea68723bd7e1cd9289e8592a7cc087c46
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798887"
---
# <a name="known-issues-in-excel-xll-development"></a>Excel �A�h�C�� (XLL) �J���ɂ�������m�̖��

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
���̃g�s�b�N�ł́AMicrosoft Excel �ł� XLL �J���ő�������\���̂�����m�̖��ɂ��Đ�����܂��B
  
## <a name="unregistering-xll-commands-and-functions"></a>XLL �̃R�}���h����ъ֐���o�^�������

登録すると、XLL 関数やコマンド、Excel は、リソースの新しい名前を作成し、その名前を持つ DLL 関数への参照を関連付けます。 名前は、4 番目の引数では、 *pxFunctionText* 、 [xlfRegister](xlfregister-form-1.md)関数から取得されます。 この名前がワークシート名を管理するための標準のダイアログ ボックスから非表示にします。 関数やコマンドの登録を解除するには、 [xlfSetName](xlfsetname.md)関数を使用して、名前を渡すことが、定義が渡されていない名前を削除してください。 ただし、バグによりこの関数ウィザードの一覧から名前を削除します。 
  
## <a name="argument-description-string-truncation-in-the-function-wizard"></a>�֐��E�B�U�[�h�ɂ���������̐��������̐؂�̂�

*PxArgumentHelp1*パラメーターと**xlfRegister**関数の後続のすべてのパラメーターは、XLL 関数の引数に対応するオプションの文字列です。 関数ウィザードには、これらの引数の作成] ダイアログ ボックスでヘルプを提供するが表示されます。 Excel では、ダイアログ ボックスで表示する場合の 1 つまたは 2 つの文字で最後の引数に対応する文字列が切り捨てられます。 最終的な文字列の末尾に 1 つまたは 2 つのスペースを追加することによってこれを回避できます。 
  
## <a name="binary-name-scope-limitation"></a>�o�C�i�����̃X�R�[�v����

バイナリ名とそのデータは、作成された時点でアクティブだったワークシートが再度アクティブになったときにのみ取得できます。ワークシート関数では、ワークブック内のワークシートをアクティブにすることはできないため (コマンドでのみ可能)、バイナリ名の適用は非常に制限されています。特定のワークシートからのみ呼び出されるコマンドがあれば、バイナリ名を使用してコマンドに関するデータを格納することもできます。
  
## <a name="xlset-and-workbooks-with-array-formulas"></a>xlSet �Ɣz�񐔎���܂ރ��[�N�u�b�N

Excel 2003 およびそれ以前のバージョンでは、 [xlSet 関数](xlset.md)ではない、アクティブなワークシート、作業中のワークシートと同じ範囲が配列数式を含むワークシート上の範囲に値を代入しようとする場合を失敗します。 この例では、「配列の一部を変更することはできません」メッセージが表示されます。 これは、Excel 2007 で修正されました。 
  
## <a name="circular-references-are-tolerated-in-data-tables"></a>�f�[�^ �e�[�u���ŏz�Q�Ƃ��\

Excel �ł͌��݁A�f�[�^ �e�[�u���̃x�[�X�ƂȂ�v�Z�ɂ����āA���e�[�u����̒l��Q�Ƃ��Ă���ꍇ�ł�G���[�ɂȂ�܂���B���̂悤�ȃV�i���I�͂܂�Ȃ��Ƃł����A�f�[�^ �e�[�u���̒l��v�Z���鐔���̍쐬��ύX�ɂ͒��ӂ��K�v�ł��B
  
## <a name="converting-an-integer-xloper12-to-an-xloper"></a>���� XLOPER12 �� XLOPER �ɕϊ�����

�����^ **xltypeInt** �́A **XLOPER12** �f�[�^�^�ł� 32 �r�b�g�̕����t�������ł����A **XLOPER** �f�[�^�^�ł� 16 �r�b�g�����t�������ł��邽�߁A���� **XLOPER12** �̒l�̒��ɂ́A���� **XLOPER** �Ɋ܂߂��Ȃ���̂����蓾�܂��BExcel ����ł��̃f�[�^�^��ϊ�����ꍇ�́A�f�[�^�^�𕂓������_ **xltypeNum** **XLOPER** �ɕϊ����Ă��̖�������܂��B
  
�t���[�����[�N�֐� [XLOper12ToXLOper](xloper12toxloper.md) �́A���̓���𔽉f���āAExcel ����̓���ƈ�v����悤�ɂ��܂��B���̊֐���Ăяo���ہA�Ԃ� **XLOPER** ����� **xltypeInt** �ł���Ƒz�肵�Ȃ��ł��������B **my_xloper** �^�� **xltypeNum** �̏ꍇ�� **my_xloper.val.w** ��ǂݏo���ƁAfalse �̒l���Ԃ�܂��B
  
## <a name="returning-xloper-or-xloper12-by-modifying-arguments-in-place"></a>������C���v���[�X�ŕύX���� XLOPER �܂��� XLOPER12 ��Ԃ�

Excel �ł͈�����C���v���[�X�ŕύX���āA **XLOPER** �܂��� **XLOPER12** ��Ԃ��悤�Ɋ֐���o�^���邱�Ƃ��ł��܂��B�������A **XLOPER**/ **XLOPER12** ��������������|�C���g���Ă���A���̃|�C���^�� DLL �֐��̖߂�l�ŏ㏑�������ƁAExcel �̓����� ���[�N�ɂȂ��鋰�ꂪ����܂��BExcel �ŃG���[�͕\������܂��񂪁A���ʓI�ɃN���b�V�����鋰�ꂪ����܂��B�܂��ADLL �Ŗ߂�l�p�̃����������蓖�Ă��Ă���ꍇ�AExcel �͂��̃������������悤�Ƃ��邽�߁A�����ɃA�v���P�[�V�������N���b�V�����鋰�ꂪ����܂��B���̂��߁A **XLOPER**/ **XLOPER12** �����̓C���v���[�X�ŕύX���Ȃ��ł��������B **XLOPER** ������ **XLOPER12** �����͂��ׂāA�K���ǂݎ���p�Ƃ��Ĉ����Ă��������B 
  
�ڍׂɂ��ẮA�u[Excel �̃������Ǘ�](memory-management-in-excel.md)�v��Q�Ƃ��Ă��������B
  
## <a name="see-also"></a>�֘A����



[XLOper12ToXLOper](xloper12toxloper.md)


[Excel XLL �̊J��](developing-excel-xlls.md)
  
[Excel XLL SDK API �֐����t�@�����X](excel-xll-sdk-api-function-reference.md)
  
[Excel �̃������Ǘ�](memory-management-in-excel.md)

