---
title: fDialog/fDialog12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDialog
- fDialog12
keywords:
- fdialog function [excel 2007],fDialog12 function [Excel 2007]
localization_priority: Normal
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 554b76d2d316110286e83158acfff33aa68e19c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798875"
---
# <a name="fdialogfdialog12"></a><span data-ttu-id="f435e-104">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="f435e-104">fDialog/fDialog12</span></span>

 <span data-ttu-id="f435e-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f435e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f435e-p101">ユーザー定義コマンドの例で、C API のダイアログ ボックスの機能を使用して、DLL 内で Microsoft Excel UDD (ユーザー定義のダイアログ ボックス) を作成する方法を説明します。GENERIC.xll が読み込まれると、このコマンドにアクセスするのに使用するユーザー定義メニュー [Generic] を作成します。</span><span class="sxs-lookup"><span data-stu-id="f435e-p101">Example user-defined command that demonstrates how to create a Microsoft Excel UDD (user-defined dialog box) within a DLL by using the dialog box capabilities in the C API. When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="f435e-108">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="f435e-108">Parameters</span></span>

<span data-ttu-id="f435e-109">���̊֐��ɂ̓p�����[�^�[�͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="f435e-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="f435e-110">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="f435e-110">Property value/Return value</span></span>

<span data-ttu-id="f435e-111">���̊֐��́A��� 1 ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="f435e-111">The function always returns 1.</span></span>
  
### <a name="example"></a><span data-ttu-id="f435e-112">��</span><span class="sxs-lookup"><span data-stu-id="f435e-112">Example</span></span>

<span data-ttu-id="f435e-113">���̊֐��̃\�[�X �R�[�h�ɂ��ẮA `\SAMPLES\GENERIC\GENERIC.C` ��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="f435e-113">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f435e-114">�֘A����</span><span class="sxs-lookup"><span data-stu-id="f435e-114">See also</span></span>



[<span data-ttu-id="f435e-115">�ėp DLL �̊֐�</span><span class="sxs-lookup"><span data-stu-id="f435e-115">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

