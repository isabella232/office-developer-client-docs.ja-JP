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
ms.openlocfilehash: b16730681b5414f28ae45be7195b4fa551bf0e82
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591990"
---
# <a name="imapisupportmodifyprofile"></a><span data-ttu-id="c90ec-103">IMAPISupport::ModifyProfile</span><span class="sxs-lookup"><span data-stu-id="c90ec-103">IMAPISupport::ModifyProfile</span></span>

  
  
<span data-ttu-id="c90ec-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c90ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c90ec-105">永続的なプロファイルのセクションを保存するメッセージを変更します。</span><span class="sxs-lookup"><span data-stu-id="c90ec-105">Makes changes to a message store profile section permanent.</span></span>
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c90ec-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="c90ec-106">Parameters</span></span>

 <span data-ttu-id="c90ec-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c90ec-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c90ec-108">[in]メッセージの種類を示すフラグのビットマスクを格納します。</span><span class="sxs-lookup"><span data-stu-id="c90ec-108">[in] A bitmask of flags that indicates the type of message store.</span></span> <span data-ttu-id="c90ec-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="c90ec-109">The following flag can be set:</span></span>
    
<span data-ttu-id="c90ec-110">MDB_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="c90ec-110">MDB_TEMPORARY</span></span> 
  
> <span data-ttu-id="c90ec-111">メッセージ ・ ストアでは、一時的なものと、メッセージ ストアのテーブルに追加できませんする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c90ec-111">The message store is temporary and should not be added to the message store table.</span></span> <span data-ttu-id="c90ec-112">MDB_TEMPORARY を設定すると、 **ModifyProfile**はすぐに S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="c90ec-112">When MDB_TEMPORARY is set, **ModifyProfile** returns S_OK immediately.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c90ec-113">�߂�l</span><span class="sxs-lookup"><span data-stu-id="c90ec-113">Return value</span></span>

<span data-ttu-id="c90ec-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="c90ec-114">S_OK</span></span> 
  
> <span data-ttu-id="c90ec-115">プロファイル セクションへの変更は成功しました。</span><span class="sxs-lookup"><span data-stu-id="c90ec-115">The changes to the profile section were successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c90ec-116">注釈</span><span class="sxs-lookup"><span data-stu-id="c90ec-116">Remarks</span></span>

<span data-ttu-id="c90ec-117">メッセージ ストア プロバイダーのサポート オブジェクトの**IMAPISupport::ModifyProfile**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="c90ec-117">The **IMAPISupport::ModifyProfile** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="c90ec-118">メッセージのストア プロバイダーの呼び出し**ModifyProfile**プロファイル情報を変更するのには MAPI メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="c90ec-118">Message store providers call **ModifyProfile** to prompt MAPI to modify their profile information.</span></span> 
  
 <span data-ttu-id="c90ec-119">**ModifyProfile**は、インストールされているメッセージ ストア プロバイダーのリソースの一覧を呼び出し元のプロバイダーに関連付けられているプロファイルのセクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="c90ec-119">**ModifyProfile** adds the profile section that is associated with the calling provider to the list of installed message store provider resources.</span></span> <span data-ttu-id="c90ec-120">[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)メソッドを介してクライアントには、メッセージ ストアのテーブルに登録して、ダイアログ ボックスの表示を開くには、メッセージ ストアが発生します。</span><span class="sxs-lookup"><span data-stu-id="c90ec-120">This causes the message store to be listed in the message store table, which is available to clients through the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method, and to be opened without the display of a dialog box.</span></span> 
  
<span data-ttu-id="c90ec-121">MDB_TEMPORARY フラグが設定されている場合、MAPI は何し、メソッドは、すぐに S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="c90ec-121">If the MDB_TEMPORARY flag is set, MAPI does nothing and the method returns immediately with S_OK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c90ec-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="c90ec-122">See also</span></span>



[<span data-ttu-id="c90ec-123">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="c90ec-123">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="c90ec-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c90ec-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

