---
title: xlfUnregister (�`�� 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister (Form 2)
keywords:
- xlfunregister [excel 2007]
localization_priority: Normal
ms.assetid: 39c6eba7-ba41-4e7b-9a28-2b662378ff5a
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: e0154e380b65b8c57e7e96a98ef131e26b49e203
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798996"
---
# <a name="xlfunregister-form-2"></a>xlfUnregister (�`�� 2)

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Microsoft Excel �ɂ���Ă��ꎩ�̂��Ăяo����� DLL �� XLL �R�}���h����Ăяo�����Ƃ��ł��܂��B����́A **UNREGISTER** �� Excel XLM �}�N�� �V�[�g����Ăяo���̂Ɠ����ł��B 
  
**xlfUnregister** �́A2 �̌`���ŌĂяo�����Ƃ��ł��܂��B 
  
- �`�� 1:�X�̃R�}���h��֐��̓o�^�������܂��B
    
- �`�� 2:XLL �̃A�����[�h�Ɣ�A�N�e�B�x�[�g����s���܂��B
    
�`�� 2 �ŌĂяo�����ƁA���̊֐��� DLL ��R�[�h ���\�[�X�̊��S�ȃA�����[�h��������܂��B�ʂ̃}�N���Ō��ݎg���Ă��Ă�ADLL ��̂��ׂĂ̊֐��̓o�^�������܂��B�֐��̎g�p�ɂ��čl������܂���B���̊֐��� **xlAutoClose** ��Ăяo���Ă���ADLL ��̂��ׂĂ̊֐��̓o�^�������܂��B
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>�p�����[�^�[

_pxModuleText_(**xltypeStr**)
  
DLL �̖��O�B
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

成功した場合は、 **TRUE** (**xltypeBool**) を返します。 失敗した場合は、 **FALSE**が返されます。
  
## <a name="remarks"></a>����

> [!NOTE] 
> 呼び出さないで関数の形式はこの[xlAutoClose](xlautoclose.md)の実装から 1 つの単純な関数呼び出しを使用して、DLL のリソースのすべての登録を解除しようとしてください。 これ**xlAutoClose**とスタック オーバーフローの再帰的な呼び出しにつながります。 
  
### <a name="remember-to-delete-names"></a>名前を削除することを忘れないでください。

_pxFunctionText_ ������ **xlfRegister** �Ɏw�肷��ꍇ�́ADLL �̊֐��ƃR�}���h�̓o�^���ɁA���ꂼ��ɂ��� 2 �ڂ̈�����ȗ����� **xlfSetName** ��Ăяo���A�֐����֐��E�B�U�[�h�ɕ\������Ȃ��悤�ɖ��O�𖾎��I�ɍ폜����K�v������܂��B�ڂ����́u [Excel �A�h�C�� (XLL) �J���ɂ�������m�̖��](known-issues-in-excel-xll-development.md)�v��������������B
  
## <a name="see-also"></a>�֘A����

- [xlfRegister (�`�� 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [xlfUnregister (�`�� 1)](xlfunregister-form-1.md)
- [�d�v�Ŗ�ɗ��� C API XLM �֐�](essential-and-useful-c-api-xlm-functions.md)

