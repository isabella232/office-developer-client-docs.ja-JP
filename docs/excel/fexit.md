---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- fexit function [excel 2007]
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 3abb5cd68a45fbcd16665dbc4d492d764bbd315e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798870"
---
# <a name="fexit"></a><span data-ttu-id="eb0a3-104">fExit</span><span class="sxs-lookup"><span data-stu-id="eb0a3-104">fExit</span></span>

 <span data-ttu-id="eb0a3-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="eb0a3-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="eb0a3-p101">GENERIC.xll をアンロードするユーザー定義コマンドの例。GENERIC.xll が読み込まれると、このコマンドにアクセスするユーザー定義メニュー [Generic] を作成します。 </span><span class="sxs-lookup"><span data-stu-id="eb0a3-p101">Example user-defined command that unloads GENERIC.xll. When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span> 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a><span data-ttu-id="eb0a3-108">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="eb0a3-108">Parameters</span></span>

<span data-ttu-id="eb0a3-109">���̊֐��ɂ̓p�����[�^�[�͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="eb0a3-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="eb0a3-110">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="eb0a3-110">Property value/Return value</span></span>

<span data-ttu-id="eb0a3-111">���̊֐��́A��� 1 ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="eb0a3-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eb0a3-112">����</span><span class="sxs-lookup"><span data-stu-id="eb0a3-112">Remarks</span></span>

<span data-ttu-id="eb0a3-p102">����� GENERIC.xll �I�����邽�߂Ƀ��[�U�[���J�n���郋�[�`UNREGISTER("GENERIC.XLL")`UNREGISTER("GENERIC.XLL")\` ��Ăяo�����Ƃ͔����K�v������܂��B����͋����I�ɁA���� DLL ��̂��ׂĂ̊֐���o�^������܂��B�����̊֐������̂����ꂩ�ɓo�^����Ă���ꍇ������ł��B���̑���ɁA������ 1 �̊֐���o�^������܂��B</span><span class="sxs-lookup"><span data-stu-id="eb0a3-p102">This is a user-initiated routine to exit GENERIC.xll You should avoid simply calling  `UNREGISTER("GENERIC.XLL")` in this function. This would forcefully unregister all the functions in this DLL, even if they are registered somewhere else. Instead, unregister the functions one at a time.</span></span> 
  
### <a name="example"></a><span data-ttu-id="eb0a3-116">��</span><span class="sxs-lookup"><span data-stu-id="eb0a3-116">Example</span></span>

<span data-ttu-id="eb0a3-117">���̊֐��̃\�[�X �R�[�h�ɂ��ẮA `\SAMPLES\GENERIC\GENERIC.C` ��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="eb0a3-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eb0a3-118">�֘A����</span><span class="sxs-lookup"><span data-stu-id="eb0a3-118">See also</span></span>



[<span data-ttu-id="eb0a3-119">�ėp DLL �̊֐�</span><span class="sxs-lookup"><span data-stu-id="eb0a3-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

