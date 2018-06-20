---
title: IMAPISupportModifyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyProfile
api_type:
- COM
ms.assetid: 33bef4ea-d6c0-4455-b95d-4b29edb9c0bc
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 98e6331d5a9e52d5ae73ed12d8c045bdf226c2c4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800750"
---
# <a name="imapisupportmodifyprofile"></a><span data-ttu-id="e7475-103">IMAPISupport::ModifyProfile</span><span class="sxs-lookup"><span data-stu-id="e7475-103">IMAPISupport::ModifyProfile</span></span>

  
  
<span data-ttu-id="e7475-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e7475-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e7475-105">永続的なプロファイルのセクションを保存するメッセージを変更します。</span><span class="sxs-lookup"><span data-stu-id="e7475-105">Makes changes to a message store profile section permanent.</span></span>
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e7475-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="e7475-106">Parameters</span></span>

 <span data-ttu-id="e7475-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e7475-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e7475-108">[in]メッセージの種類を示すフラグのビットマスクを格納します。</span><span class="sxs-lookup"><span data-stu-id="e7475-108">[in] A bitmask of flags that indicates the type of message store.</span></span> <span data-ttu-id="e7475-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="e7475-109">The following flag can be set:</span></span>
    
<span data-ttu-id="e7475-110">MDB_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="e7475-110">MDB_TEMPORARY</span></span> 
  
> <span data-ttu-id="e7475-111">メッセージ ・ ストアでは、一時的なものと、メッセージ ストアのテーブルに追加できませんする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7475-111">The message store is temporary and should not be added to the message store table.</span></span> <span data-ttu-id="e7475-112">MDB_TEMPORARY を設定すると、 **ModifyProfile**はすぐに S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="e7475-112">When MDB_TEMPORARY is set, **ModifyProfile** returns S_OK immediately.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e7475-113">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e7475-113">Return value</span></span>

<span data-ttu-id="e7475-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="e7475-114">S_OK</span></span> 
  
> <span data-ttu-id="e7475-115">プロファイル セクションへの変更は成功しました。</span><span class="sxs-lookup"><span data-stu-id="e7475-115">The changes to the profile section were successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e7475-116">備考</span><span class="sxs-lookup"><span data-stu-id="e7475-116">Remarks</span></span>

<span data-ttu-id="e7475-117">メッセージ ストア プロバイダーのサポート オブジェクトの**IMAPISupport::ModifyProfile**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="e7475-117">The **IMAPISupport::ModifyProfile** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="e7475-118">メッセージのストア プロバイダーの呼び出し**ModifyProfile**プロファイル情報を変更するのには MAPI メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="e7475-118">Message store providers call **ModifyProfile** to prompt MAPI to modify their profile information.</span></span> 
  
 <span data-ttu-id="e7475-119">**ModifyProfile**は、インストールされているメッセージ ストア プロバイダーのリソースの一覧を呼び出し元のプロバイダーに関連付けられているプロファイルのセクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="e7475-119">**ModifyProfile** adds the profile section that is associated with the calling provider to the list of installed message store provider resources.</span></span> <span data-ttu-id="e7475-120">[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)メソッドを介してクライアントには、メッセージ ストアのテーブルに登録して、ダイアログ ボックスの表示を開くには、メッセージ ストアが発生します。</span><span class="sxs-lookup"><span data-stu-id="e7475-120">This causes the message store to be listed in the message store table, which is available to clients through the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method, and to be opened without the display of a dialog box.</span></span> 
  
<span data-ttu-id="e7475-121">MDB_TEMPORARY フラグが設定されている場合、MAPI は何し、メソッドは、すぐに S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="e7475-121">If the MDB_TEMPORARY flag is set, MAPI does nothing and the method returns immediately with S_OK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e7475-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="e7475-122">See also</span></span>



[<span data-ttu-id="e7475-123">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="e7475-123">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="e7475-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e7475-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

