---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- xldefinebinaryname function [excel 2007]
localization_priority: Normal
ms.assetid: e3e8f91b-cc31-4f09-9941-f950ae96820a
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 14515cc262ea398a9f200c0de3a1f6b64c758b3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798962"
---
# <a name="xldefinebinaryname"></a>xlDefineBinaryName

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
**XltypeBigData** **XLOPER**の永続的なストレージを割り当てるために使用/ **XLOPER12**。 定義されているバイナリの名前を使用してデータはブックと共に保存し、名前でいつでもアクセスできます。 詳細については、「バイナリ名前スコープの制限」 [Excel XLL 開発で既知問題](known-issues-in-excel-xll-development.md)を参照してください。
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a>�p�����[�^�[

 _pxName_(**xltypeStr**)
  
�f�[�^�̖��O��w�肷�镶����B������́A��`���ꂽ���O�Ɠ��������̐����ɏ]���܂��B
  
 _pxData_(**xltypeBigData**)
  
�i�[����f�[�^��w�肷�� Bigdata �\���́B���̊֐���Ăяo���ƁA **bigdata** �\���̂� **lpbData** �����o�[�͖��O����`����Ă���f�[�^��|�C���g����K�v������܂��B�܂��A **cbData** �����o�[�ɂ́A�f�[�^�̒��� (�o�C�g�P��) ���܂܂�Ă���K�v������܂��B 
  
_PxData_引数が指定された (**xltypeMissing**) でない場合は、 _pxName_で指定された名前付きの割り当てが削除されます。 
  
## <a name="see-also"></a>関連項目



[xlGetBinaryName](xlgetbinaryname.md)


[DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Excel �A�h�C�� (XLL) �J���ɂ�������m�̖��](known-issues-in-excel-xll-development.md)

