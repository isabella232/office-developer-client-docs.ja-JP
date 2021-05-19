---
title: IMAPIControlActivate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.Activate
api_type:
- COM
ms.assetid: 2b641030-2429-4217-a648-0a9f3d1a1b29
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d3b47e423daf428c67761d13deef1ae0858c91c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418016"
---
# <a name="imapicontrolactivate"></a><span data-ttu-id="c346f-103">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="c346f-103">IMAPIControl::Activate</span></span>

  
  
<span data-ttu-id="c346f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c346f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c346f-105">クライアント アプリケーション のユーザーがボタン コントロールをクリックすると、ダイアログ ボックスの表示やプログラムによる操作の開始などのタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="c346f-105">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a><span data-ttu-id="c346f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c346f-106">Parameters</span></span>

 <span data-ttu-id="c346f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c346f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c346f-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="c346f-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="c346f-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c346f-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="c346f-110">[in]ボタン コントロールが表示されるダイアログ ボックスの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="c346f-110">[in] A handle to the parent window of the dialog box on which the button control appears.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c346f-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="c346f-111">Return value</span></span>

<span data-ttu-id="c346f-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="c346f-112">S_OK</span></span> 
  
> <span data-ttu-id="c346f-113">ボタン コントロールが正常にアクティブ化されました。</span><span class="sxs-lookup"><span data-stu-id="c346f-113">The button control was successfully activated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c346f-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c346f-114">Remarks</span></span>

<span data-ttu-id="c346f-115">**IMAPIControl::Activate** メソッドは、ユーザーがボタン コントロールをクリックした後にタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="c346f-115">The **IMAPIControl::Activate** method performs tasks following a user's click of the button control.</span></span> <span data-ttu-id="c346f-116">クリックが発生した後、表示テーブルの処理の一環として、MAPI は[IMAPIControl::GetState](imapicontrol-getstate.md)を最初に呼び出した後に Activate を呼び出し、ボタンが有効になっているかどうかを判断します。 </span><span class="sxs-lookup"><span data-stu-id="c346f-116">After the click occurs, as part of the processing of the display table, MAPI makes a call to **Activate** after first calling [IMAPIControl::GetState](imapicontrol-getstate.md) to determine whether the button is enabled.</span></span> 
  
<span data-ttu-id="c346f-117">**Activate** および他の [IMAPIControl : IUnknown](imapicontroliunknown.md)メソッドを実装する方法の詳細については [、「Control Object Implementation」を参照してください](control-object-implementation.md)。</span><span class="sxs-lookup"><span data-stu-id="c346f-117">For more information about how to implement **Activate** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c346f-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="c346f-118">See also</span></span>



[<span data-ttu-id="c346f-119">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="c346f-119">IMAPIControl::GetState</span></span>](imapicontrol-getstate.md)
  
[<span data-ttu-id="c346f-120">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c346f-120">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

