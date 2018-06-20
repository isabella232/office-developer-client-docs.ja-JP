---
title: DIALOGMsgProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- DIALOGMsgProc
keywords:
- dialogmsgproc function [excel 2007]
localization_priority: Normal
ms.assetid: 9a538e83-ba34-4806-bb8c-7cda3beb6b66
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 3a69d192babbcf0419850e203f51d8cfd81cdef6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798773"
---
# <a name="dialogmsgproc"></a><span data-ttu-id="35244-104">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="35244-104">DIALOGMsgProc</span></span>

<span data-ttu-id="35244-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="35244-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="35244-106">この手順が関連付けられているネイティブの Windows のダイアログ ボックスでその[fShowDialog](fshowdialog.md)が表示されます。</span><span class="sxs-lookup"><span data-stu-id="35244-106">This procedure is associated with the native Windows dialog box that [fShowDialog](fshowdialog.md) displays.</span></span> <span data-ttu-id="35244-107">ダイアログ ボックスのボタン、入力フィールド、またはコントロールのいずれかの操作時に発生するイベント (メッセージ) の windows と呼ばれるサービス ルーチンが用意されています。</span><span class="sxs-lookup"><span data-stu-id="35244-107">It provides the service routines called by Windows for the events (messages) that occur when the user operates one of the dialog box's buttons, entry fields, or controls.</span></span> 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="35244-108">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="35244-108">Parameters</span></span>

 <span data-ttu-id="35244-109">_hWndDlg_(**HWND**)</span><span class="sxs-lookup"><span data-stu-id="35244-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="35244-110">�_�C�A���O �{�b�N�X�� HWND Windows �n���h����܂�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="35244-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="35244-111">_メッセージ_(**UINT**)</span><span class="sxs-lookup"><span data-stu-id="35244-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="35244-112">�������b�Z�[�W</span><span class="sxs-lookup"><span data-stu-id="35244-112">The message to respond to.</span></span>
  
 <span data-ttu-id="35244-113">_wParam_(**WPARAM**)</span><span class="sxs-lookup"><span data-stu-id="35244-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="35244-114">_lParam_(**LPARAM**)</span><span class="sxs-lookup"><span data-stu-id="35244-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="35244-115">Windows ���n��������</span><span class="sxs-lookup"><span data-stu-id="35244-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="35244-116">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="35244-116">Property value/Return value</span></span>

 <span data-ttu-id="35244-117">���b�Z�[�W����������Ă���ꍇ�� **TRUE**�A�������̏ꍇ�� **FALSE**�B</span><span class="sxs-lookup"><span data-stu-id="35244-117">**TRUE** if message processed, **FALSE** if not.</span></span> 
  
### <a name="example"></a><span data-ttu-id="35244-118">��</span><span class="sxs-lookup"><span data-stu-id="35244-118">Example</span></span>

<span data-ttu-id="35244-119">���̊֐��̃\�[�X �R�[�h�ɂ��ẮA `\SAMPLES\GENERIC\GENERIC.C` ��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="35244-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="35244-120">�֘A����</span><span class="sxs-lookup"><span data-stu-id="35244-120">See also</span></span>



[<span data-ttu-id="35244-121">�ėp DLL �̊֐�</span><span class="sxs-lookup"><span data-stu-id="35244-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

