---
title: アカウント管理 API の概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: eb6b921d-ecf8-3ce5-87ba-ac1632416b05
description: アカウント管理 API では、アカウント情報へのアクセスを提供し、アカウントの変更の通知をサポートします。 この API のクライアントとしてメール プロバイダーの次の操作を行います。
ms.openlocfilehash: 678143def25395c47f1c17cc99dcdcd1fb145e1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799297"
---
# <a name="about-the-account-management-api"></a><span data-ttu-id="c69fb-104">アカウント管理 API の概要</span><span class="sxs-lookup"><span data-stu-id="c69fb-104">About the Account Management API</span></span>

<span data-ttu-id="c69fb-105">アカウント管理 API では、アカウント情報へのアクセスを提供し、アカウントの変更の通知をサポートします。</span><span class="sxs-lookup"><span data-stu-id="c69fb-105">The Account Management API provides access to account information and supports notifications of account changes.</span></span> <span data-ttu-id="c69fb-106">この API のクライアントとしてメール プロバイダーの次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="c69fb-106">As clients of this API, mail providers do the following:</span></span>
  
1. <span data-ttu-id="c69fb-107">アカウントへのアクセスを管理し、アカウントの変更に関する通知を設定するには、 [IOlkAccountManager](iolkaccountmanager.md)を使用します。</span><span class="sxs-lookup"><span data-stu-id="c69fb-107">Use [IOlkAccountManager](iolkaccountmanager.md) to manage access to accounts and set up notifications about account changes.</span></span> 
    
2. <span data-ttu-id="c69fb-108">実装し、アカウントの変更に関する通知を送信する[IOlkAccountNotify](iolkaccountnotify.md)を使用します。</span><span class="sxs-lookup"><span data-stu-id="c69fb-108">Implement and use [IOlkAccountNotify](iolkaccountnotify.md) to send notifications about account changes.</span></span> 
    
3. <span data-ttu-id="c69fb-109">[IOlkEnum](iolkenum.md)を使用して、アカウントを列挙します。</span><span class="sxs-lookup"><span data-stu-id="c69fb-109">Use [IOlkEnum](iolkenum.md) to enumerate accounts.</span></span> 
    
4. <span data-ttu-id="c69fb-110">取得し、プロパティとその他のアカウント情報を設定するには、 [IOlkAccount](iolkaccount.md)を使用します。</span><span class="sxs-lookup"><span data-stu-id="c69fb-110">Use [IOlkAccount](iolkaccount.md) to get and set properties and other information about an account.</span></span> <span data-ttu-id="c69fb-111">クライアントでは、個別のアカウントにアクセスするには、 [IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md)または[IOlkEnum::GetNext](iolkenum-getnext.md)では、このインターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="c69fb-111">Clients obtain this interface through [IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) or [IOlkEnum::GetNext](iolkenum-getnext.md) to access an individual account.</span></span> 
    
5. <span data-ttu-id="c69fb-112">実装し、アカウントのプロファイルの名前と現在の MAPI セッションを取得するなど、アカウント マネージャー ヘルパー機能を提供する[IOlkAccountHelper](iolkaccounthelper.md)を使用します。</span><span class="sxs-lookup"><span data-stu-id="c69fb-112">Implement and use [IOlkAccountHelper](iolkaccounthelper.md) to provide the account manager helper functionality, including getting an account's profile name and the current MAPI session.</span></span> 
    
6. <span data-ttu-id="c69fb-113">実装し、 **IOlkAccountManager**、 **IOlkAccountNotify**、および**IOlkAccount**でのエラーに関する追加情報を提供する[IOlkErrorUnknown](iolkerrorunknown.md)を使用します。</span><span class="sxs-lookup"><span data-stu-id="c69fb-113">Implement and use [IOlkErrorUnknown](iolkerrorunknown.md) to provide extra information about an error in **IOlkAccountManager**, **IOlkAccountNotify**, and **IOlkAccount**.</span></span> 

##  <a name="account-management-api-components"></a><span data-ttu-id="c69fb-114">アカウント管理 API のコンポーネント</span><span class="sxs-lookup"><span data-stu-id="c69fb-114">Account Management API components</span></span>

<span data-ttu-id="c69fb-115">アカウント管理 API は、次の定義、データ型、インターフェイス、プロパティ、およびプロパティの名前を提供します。</span><span class="sxs-lookup"><span data-stu-id="c69fb-115">The Account Management API provides the following definitions, data types, interfaces, named properties, and properties.</span></span>
  
### <a name="definitions"></a><span data-ttu-id="c69fb-116">定義</span><span class="sxs-lookup"><span data-stu-id="c69fb-116">Definitions</span></span>
  
- [<span data-ttu-id="c69fb-117">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="c69fb-117">Constants (Account management API)</span></span>](constants-account-management-api.md)
    
### <a name="data-types"></a><span data-ttu-id="c69fb-118">データ型</span><span class="sxs-lookup"><span data-stu-id="c69fb-118">Data types</span></span>
  
- [<span data-ttu-id="c69fb-119">ACCT_BIN</span><span class="sxs-lookup"><span data-stu-id="c69fb-119">ACCT_BIN</span></span>](acct_bin.md)
    
- [<span data-ttu-id="c69fb-120">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="c69fb-120">ACCT_VARIANT</span></span>](acct_variant.md)
    
### <a name="interfaces"></a><span data-ttu-id="c69fb-121">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="c69fb-121">Interfaces</span></span>
  
- [<span data-ttu-id="c69fb-122">IOlkAccount</span><span class="sxs-lookup"><span data-stu-id="c69fb-122">IOlkAccount</span></span>](iolkaccount.md)
    
- [<span data-ttu-id="c69fb-123">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="c69fb-123">IOlkAccountHelper</span></span>](iolkaccounthelper.md)
    
- [<span data-ttu-id="c69fb-124">IOlkAccountManager</span><span class="sxs-lookup"><span data-stu-id="c69fb-124">IOlkAccountManager</span></span>](iolkaccountmanager.md)
    
- [<span data-ttu-id="c69fb-125">IOlkAccountNotify</span><span class="sxs-lookup"><span data-stu-id="c69fb-125">IOlkAccountNotify</span></span>](iolkaccountnotify.md)
    
- [<span data-ttu-id="c69fb-126">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="c69fb-126">IOlkEnum</span></span>](iolkenum.md)
    
- [<span data-ttu-id="c69fb-127">IOlkErrorUnknown</span><span class="sxs-lookup"><span data-stu-id="c69fb-127">IOlkErrorUnknown</span></span>](iolkerrorunknown.md)
    
### <a name="named-properties"></a><span data-ttu-id="c69fb-128">名前付きプロパティ</span><span class="sxs-lookup"><span data-stu-id="c69fb-128">Named properties</span></span>
  
- [<span data-ttu-id="c69fb-129">PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="c69fb-129">PidLidInternetAccountName</span></span>](pidlidinternetaccountname.md)
    
- [<span data-ttu-id="c69fb-130">PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="c69fb-130">PidLidInternetAccountStamp</span></span>](pidlidinternetaccountstamp.md)
    
### <a name="properties"></a><span data-ttu-id="c69fb-131">プロパティ</span><span class="sxs-lookup"><span data-stu-id="c69fb-131">Properties</span></span>
  
- [<span data-ttu-id="c69fb-132">PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="c69fb-132">PidTagNextSendAcct</span></span>](pidtagnextsendacct.md)
    
- [<span data-ttu-id="c69fb-133">PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="c69fb-133">PidTagPrimarySendAccount</span></span>](pidtagprimarysendaccount.md)
    
- [<span data-ttu-id="c69fb-134">PROP_ACCT_DELIVERY_FOLDER</span><span class="sxs-lookup"><span data-stu-id="c69fb-134">PROP_ACCT_DELIVERY_FOLDER</span></span>](prop_acct_delivery_folder.md)
    
- [<span data-ttu-id="c69fb-135">PROP_ACCT_DELIVERY_STORE</span><span class="sxs-lookup"><span data-stu-id="c69fb-135">PROP_ACCT_DELIVERY_STORE</span></span>](prop_acct_delivery_store.md)
    
- [<span data-ttu-id="c69fb-136">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="c69fb-136">PROP_ACCT_ID</span></span>](prop_acct_id.md)
    
- [<span data-ttu-id="c69fb-137">PROP_ACCT_IS_EXCH</span><span class="sxs-lookup"><span data-stu-id="c69fb-137">PROP_ACCT_IS_EXCH</span></span>](prop_acct_is_exch.md)
    
- [<span data-ttu-id="c69fb-138">PROP_ACCT_NAME</span><span class="sxs-lookup"><span data-stu-id="c69fb-138">PROP_ACCT_NAME</span></span>](prop_acct_name.md)
    
- [<span data-ttu-id="c69fb-139">PROP_ACCT_PREFERENCES_UID</span><span class="sxs-lookup"><span data-stu-id="c69fb-139">PROP_ACCT_PREFERENCES_UID</span></span>](prop_acct_preferences_uid.md)
    
- [<span data-ttu-id="c69fb-140">PROP_ACCT_SEND_STAMP</span><span class="sxs-lookup"><span data-stu-id="c69fb-140">PROP_ACCT_SEND_STAMP</span></span>](prop_acct_send_stamp.md)
    
- [<span data-ttu-id="c69fb-141">PROP_ACCT_SENTITEMS_EID</span><span class="sxs-lookup"><span data-stu-id="c69fb-141">PROP_ACCT_SENTITEMS_EID</span></span>](prop_acct_sentitems_eid.md)
    
- [<span data-ttu-id="c69fb-142">PROP_ACCT_STAMP</span><span class="sxs-lookup"><span data-stu-id="c69fb-142">PROP_ACCT_STAMP</span></span>](prop_acct_stamp.md)
    
- [<span data-ttu-id="c69fb-143">PROP_ACCT_USER_EMAIL_ADDR</span><span class="sxs-lookup"><span data-stu-id="c69fb-143">PROP_ACCT_USER_EMAIL_ADDR</span></span>](prop_acct_user_email_addr.md)
    
- [<span data-ttu-id="c69fb-144">PROP_ACCT_USER_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="c69fb-144">PROP_ACCT_USER_DISPLAY_NAME</span></span>](prop_acct_user_display_name.md)
    
- [<span data-ttu-id="c69fb-145">PROP_MAPI_EMSMDB_UID</span><span class="sxs-lookup"><span data-stu-id="c69fb-145">PROP_MAPI_EMSMDB_UID</span></span>](prop_mapi_emsmdb_uid.md)
    
- [<span data-ttu-id="c69fb-146">PROP_MAPI_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c69fb-146">PROP_MAPI_IDENTITY_ENTRYID</span></span>](prop_mapi_identity_entryid.md)
    
- [<span data-ttu-id="c69fb-147">PROP_MAPI_TRANSPORT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="c69fb-147">PROP_MAPI_TRANSPORT_FLAGS</span></span>](prop_mapi_transport_flags.md)
    

