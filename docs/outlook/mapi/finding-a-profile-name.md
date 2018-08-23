---
title: プロファイル名の検索
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18df25b7-16b7-44cd-a9a0-5276966c1fd4
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a32c73f8a907b371c4d0f1c07050d44fd45801ec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576289"
---
# <a name="finding-a-profile-name"></a><span data-ttu-id="f9541-103">プロファイル名の検索</span><span class="sxs-lookup"><span data-stu-id="f9541-103">Finding a Profile Name</span></span>

  
  
<span data-ttu-id="f9541-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9541-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9541-105">クライアントは、セッション、既定のプロファイルの名前、またはコンピューターにインストールされている別のプロファイルの名前を現在使用されているプロファイルの名前を検索する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9541-105">Clients sometimes need to find the name of the profile currently being used for the session, the name of the default profile, or the name of an alternate profile installed on the computer.</span></span>
  
<span data-ttu-id="f9541-106">セッションの実行中にプロファイルの名前を取得するためにいくつかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="f9541-106">There are a few ways to retrieve the name of a profile during the course of a session.</span></span> <span data-ttu-id="f9541-107">必ずしも 1 つのセッションで使用されているプロファイルの名前を検索する場合は、最初の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="f9541-107">If you need to find the name of a profile that is not necessarily the one being used for the session, use the first procedure.</span></span> <span data-ttu-id="f9541-108">既定のプロファイルの名前を検索する場合は、2 番目の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="f9541-108">If you need to find the name of the default profile, use the second procedure.</span></span> <span data-ttu-id="f9541-109">セッションの現在のプロファイルの名前を検索する場合は、最後の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="f9541-109">If you need to find the name of the current profile for the session, use the last procedure.</span></span> 
  
 <span data-ttu-id="f9541-110">**任意のプロファイルの名前を検索するには**</span><span class="sxs-lookup"><span data-stu-id="f9541-110">**To find the name of any profile**</span></span>
  
1. <span data-ttu-id="f9541-111">**IProfAdmin**インターフェイス ポインターを取得するために[MAPIAdminProfiles](mapiadminprofiles.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f9541-111">Call [MAPIAdminProfiles](mapiadminprofiles.md) to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="f9541-112">プロファイル テーブルにアクセスするのには[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f9541-112">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="f9541-113">プロファイル テーブルの[IMAPITable::QueryRows](imapitable-queryrows.md)メソッドを呼び出して、テーブル内の行のすべてを取得し、ターゲット ・ プロファイルを表すかどうかを確認するには、各 1 を調べる。</span><span class="sxs-lookup"><span data-stu-id="f9541-113">Call the profile table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve all of the rows in the table and examine each one to determine if it represents your target profile.</span></span> 
    
 <span data-ttu-id="f9541-114">**デフォルトのプロファイルの名前を検索するには**</span><span class="sxs-lookup"><span data-stu-id="f9541-114">**To find the name of the default profile**</span></span>
  
1. <span data-ttu-id="f9541-115">[MAPIAdminProfiles](mapiadminprofiles.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f9541-115">Call [MAPIAdminProfiles](mapiadminprofiles.md).</span></span>
    
2. <span data-ttu-id="f9541-116">プロファイル テーブルにアクセスするのには[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f9541-116">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="f9541-117">TRUE の値を持つ**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) に一致する[SPropertyRestriction](spropertyrestriction.md)構造を持つプロパティの制限を作成します。</span><span class="sxs-lookup"><span data-stu-id="f9541-117">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) with the value TRUE.</span></span>
    
4. <span data-ttu-id="f9541-118">既定のプロファイルを表すプロファイル テーブルの行を検索するのには[IMAPITable::FindRow](imapitable-findrow.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f9541-118">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the row in the profile table that represents the default profile.</span></span> <span data-ttu-id="f9541-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 列には、既定のプロファイルの名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f9541-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column contains the name of the default profile.</span></span>
    
 <span data-ttu-id="f9541-120">**現在のプロファイルの名前を検索するには**</span><span class="sxs-lookup"><span data-stu-id="f9541-120">**To find the name of the current profile**</span></span>
  
<span data-ttu-id="f9541-121">現在のプロファイルの名前を検索するには、次の手順のいずれかを行います。</span><span class="sxs-lookup"><span data-stu-id="f9541-121">To find the name of the current profile, complete one of the following steps:</span></span>
  
- <span data-ttu-id="f9541-122">現在のプロファイルのセクションのいずれかを表す[MAPIUID](mapiuid.md)の構造体がある場合は、 [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)に_lpUID_パラメーターで渡すことです。</span><span class="sxs-lookup"><span data-stu-id="f9541-122">Assuming that you have the [MAPIUID](mapiuid.md) structure representing one of the current profile's sections, pass it in the  _lpUID_ parameter to [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md).</span></span> <span data-ttu-id="f9541-123">[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを使用してプロファイル セクションの**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) のプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="f9541-123">Retrieve the profile section's **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property using its [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
    
- <span data-ttu-id="f9541-124">ステータス テーブルにアクセスし、MAPI_SUBSYSTEM に設定されて、 **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) の列を持つ行を見つけるには、 [IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f9541-124">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table and find the row that has its **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column set to MAPI_SUBSYSTEM.</span></span> <span data-ttu-id="f9541-125">この行の**PR_DISPLAY_NAME**列は、プロファイルの名前です。</span><span class="sxs-lookup"><span data-stu-id="f9541-125">The **PR_DISPLAY_NAME** column for this row is the profile name.</span></span> <span data-ttu-id="f9541-126">使用されないステータス テーブル開始時にすべてのトランスポート プロバイダーを初期化して、MAPI スプーラーが終了するまでアプリケーションをブロックするためです。</span><span class="sxs-lookup"><span data-stu-id="f9541-126">Do not use the status table during start up because it blocks an application until the MAPI spooler has finished initializing all of the transport providers.</span></span> <span data-ttu-id="f9541-127">これによって、パフォーマンスが低下します。</span><span class="sxs-lookup"><span data-stu-id="f9541-127">This can degrade your performance.</span></span> 
    

