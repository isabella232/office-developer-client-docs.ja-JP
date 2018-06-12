---
title: ���[�N�V�[�g�̎Q��
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- references [excel 2007], worksheet,worksheet references [Excel 2007],external worksheet references [Excel 2007],active worksheet [Excel 2007],current worksheet [Excel 2007],internal worksheet references [Excel 2007]
localization_priority: Normal
ms.assetid: 53406fb8-4ca5-4204-a6ad-b21ca9e6a100
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: b7089fb891c96be9182189e3a5f30057721cebbc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798966"
---
# <a name="worksheet-references"></a>���[�N�V�[�g�̎Q��

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Microsoft Excel での参照は、セルの (1 つのセルを指定できます)、または、場合によってはいくつかの非結合セルのブロックの長方形のブロックを参照するデータ型です。 内部的には、内部参照と呼ばれる、現在のシート上のセルの 1 つの参照型が使用されます。 現在のシートに含まれていない任意のセルは、外部参照と呼ばれる参照の別の型で表されます。 現在の定義の次のセクションを参照してください。
  
## <a name="active-vs-current"></a>��ƒ��ƌ���

Excel ��ŁA��ƒ��Ƃ����p��́A���[�U�[���\�����̂�̂�\���܂��B��ƒ��̃u�b�N��V�[�g�́A���[�U�[�����݉{�����̃u�b�N�⃏�[�N�V�[�g�A�܂��� Excel ����ʃA�v���P�[�V�����Ƀt�H�[�J�X���ڂ����ꍇ�ɂ́AExcel �ōŌ�Ƀt�H�[�J�X���Ă����ۂɕ\�����Ă����u�b�N�⃏�[�N�V�[�g��w���܂��B��ƒ��̃V�[�g�́A�K����ƒ��̃u�b�N��ɂ���܂��B��ƒ��̃V�[�g��ŕ����̃Z�����I�����Ă���ꍇ�́A�A�N�e�B�u �Z���Ƃ��ĔF������܂��B���ߍ��݃I�u�W�F�N�g�Ƀt�H�[�J�X����Ă���ꍇ�́A�Ō�ɑI������Z�������������A�N�e�B�u�ƂȂ�܂��B 
  
�����Ƃ�����́AExcel ���Čv�Z���Ă����̂�\���܂��B���݂̃u�b�N�ƃ��[�N�V�[�g�́A���ݍČv�Z��s���Ă���u�b�N�⃏�[�N�V�[�g��w���܂��B���݂̃V�[�g�́A�K�����݂̃u�b�N��ɂ���܂��B�Čv�Z����Ă���Z���͌��݂̃Z���ƌĂ΂�܂��B�܂��A�z�񐔎����Čv�Z����Ă���ꍇ��A���݂̃Z���ƌĂ΂�܂��B 
  
�o���Ă����ׂ��d�v�ȃ|�C���g�͎��̂Ƃ���ł��B
  
- ��ƒ��̃u�b�N��V�[�g�A�Z�����A�K��������݂̃u�b�N��V�[�g�A�Z���ɂȂ�킯�ł͂���܂��� (���݂̂�̂ł���ꍇ�����܂�)�B
    
- Visual Basic for Applications (VBA) ���W���[���� �ADLL �܂��� XLL �ɂ����āA�A�h�C���֐��́A���݂̃V�[�g��ɂ��錻�݂̃Z������Ăяo����܂��B�}���` �X���b�h�Čv�Z (MTR) �̏ꍇ�́A�����̂����ꂩ����Ăяo����܂��B
    
�u�b�N��̃Z���A�Z���͈́A�V�[�g�ɂ��Ă̏���񋟂��鑽���� Excel �̊֐��́A��ƒ��̃u�b�N�A�V�[�g�A�Z���ƁA���݂̃u�b�N�A�V�[�g�A�Z���Ƃ��ʂ��܂��B�����̑���_�́A���̃Z�N�V�����ɋL�ڂ���Ă���Ƃ���A�Z�� �u���b�N�̎Q�Ƃ�\�����߂Ɏg�p����f�[�^�^�ɂ���f����܂��B
  
## <a name="internal-and-external-worksheet-references"></a>������[�N�V�[�g����ъO�����[�N�V�[�g�̎Q��

����Q�ƂƊO���Q�Ƃ̎�ȈႢ�́A�O���Q�Ƃ̃f�[�^�^�ɂ́A���[�N�V�[�g ID �ɉ����āA�Q�Ɛ�Z���̋L�q���܂܂�Ă��邱�Ƃł��B����Q�Ƃɂ̓V�[�g�ւ̎Q�Ƃ��܂܂�Ă��܂���B�V�[�g�����݂̃V�[�g�ł��邱�Ƃ�ÖٓI�Ɏ����܂��B 
  
C API 関数の多くは、参照を返すか、参照の引数を受け取る。 引数を参照するすべての C API 関数は、 **xlSheetNm**関数は、外部参照を必要とする場合を除き、内部または外部のいずれかの参照を受け取ります。 いくつかの関数は、内部または外部のいずれかの参照のみを返します。 たとえば、C API 関数[xlfCaller](xlfcaller.md)は、定義では、現在のシートに、呼び出し元のセルへの参照を返します。 返される参照は常に内部の参照、関数は非参照型を返すことができます、関数がワークシートのセルから呼び出されません。 C API 関数[xlSheetId](xlsheetid.md)は、常に外部参照のデータ型に含まれるワークシートの ID を返します。 
  
����Q�ƌ^�ƊO���Q�ƌ^�̊Ԃ̂����̎�ȈႢ�́A�O���Q�Ƃ̃f�[�^�^�́A�����V�[�g��̕����̗��U�����Z�� �u���b�N��\�����Ƃ��\�ł���_�ł��B����Q�Ƃł́A���݂̃V�[�g�� 1 �u���b�N�݂̂�\�����Ƃ��ł��܂��B���U�����Q�Ƃ́A�͈͂̈�������C�ӂ̊֐��ɓn�����Ƃ��ł��܂��B
  
## <a name="see-also"></a>�֘A����



[Excel �v���O���~���O�̊T�O](excel-programming-concepts.md)
  
[���O�Ƒ��̃��[�N�V�[�g�̎���]������](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Excel ���[�N�V�[�g�Ǝ��̕]��](excel-worksheet-and-expression-evaluation.md)

