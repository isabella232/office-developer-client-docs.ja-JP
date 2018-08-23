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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7f330ef3099175dde88bec2de3512a3c4af1db49
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580685"
---
# <a name="imapicontrolactivate"></a><span data-ttu-id="c89d2-103">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="c89d2-103">IMAPIControl::Activate</span></span>

  
  
<span data-ttu-id="c89d2-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c89d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c89d2-105">ダイアログ ボックスを表示する、クライアント アプリケーションのユーザーは、ボタン コントロールをクリックすると、プログラムの操作を開始するなどのタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="c89d2-105">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a><span data-ttu-id="c89d2-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="c89d2-106">Parameters</span></span>

 <span data-ttu-id="c89d2-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c89d2-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c89d2-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="c89d2-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="c89d2-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c89d2-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="c89d2-110">[in]ボタン コントロールを表示するダイアログ ボックスの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="c89d2-110">[in] A handle to the parent window of the dialog box on which the button control appears.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c89d2-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="c89d2-111">Return value</span></span>

<span data-ttu-id="c89d2-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="c89d2-112">S_OK</span></span> 
  
> <span data-ttu-id="c89d2-113">ボタン コントロールが正常にアクティブ化します。</span><span class="sxs-lookup"><span data-stu-id="c89d2-113">The button control was successfully activated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c89d2-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c89d2-114">Remarks</span></span>

<span data-ttu-id="c89d2-115">**IMAPIControl::Activate**メソッドでは、次のボタン コントロールのクリックをユーザーのタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="c89d2-115">The **IMAPIControl::Activate** method performs tasks following a user's click of the button control.</span></span> <span data-ttu-id="c89d2-116">、表示された表の処理の一部として、クリックが発生した MAPI 後ボタンが有効になっているかどうかを決定する最初の呼び出し[IMAPIControl::GetState](imapicontrol-getstate.md) **をアクティブにする**呼び出しが行われます。</span><span class="sxs-lookup"><span data-stu-id="c89d2-116">After the click occurs, as part of the processing of the display table, MAPI makes a call to **Activate** after first calling [IMAPIControl::GetState](imapicontrol-getstate.md) to determine whether the button is enabled.</span></span> 
  
<span data-ttu-id="c89d2-117">**アクティブにして**、その他の実装方法の詳細については[IMAPIControl: IUnknown](imapicontroliunknown.md)メソッドは、[コントロール オブジェクトの実装](control-object-implementation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c89d2-117">For more information about how to implement **Activate** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c89d2-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="c89d2-118">See also</span></span>



[<span data-ttu-id="c89d2-119">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="c89d2-119">IMAPIControl::GetState</span></span>](imapicontrol-getstate.md)
  
[<span data-ttu-id="c89d2-120">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c89d2-120">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

