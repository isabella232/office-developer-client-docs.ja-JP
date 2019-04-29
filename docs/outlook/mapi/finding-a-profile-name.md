---
title: プロファイル名の検索
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18df25b7-16b7-44cd-a9a0-5276966c1fd4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b4efdd8d8238d4bc7e89a1153b9be34c7af76355
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407922"
---
# <a name="finding-a-profile-name"></a><span data-ttu-id="2a4a8-103">プロファイル名の検索</span><span class="sxs-lookup"><span data-stu-id="2a4a8-103">Finding a Profile Name</span></span>

  
  
<span data-ttu-id="2a4a8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a4a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a4a8-105">クライアントは、セッションで現在使用されているプロファイルの名前、既定のプロファイルの名前、またはコンピューターにインストールされている代替プロファイルの名前を検索する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="2a4a8-105">Clients sometimes need to find the name of the profile currently being used for the session, the name of the default profile, or the name of an alternate profile installed on the computer.</span></span>
  
<span data-ttu-id="2a4a8-106">セッション中にプロファイルの名前を取得するには、いくつかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="2a4a8-106">There are a few ways to retrieve the name of a profile during the course of a session.</span></span> <span data-ttu-id="2a4a8-107">セッションで使用されているものとは限らないプロファイルの名前を検索する必要がある場合は、最初の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="2a4a8-107">If you need to find the name of a profile that is not necessarily the one being used for the session, use the first procedure.</span></span> <span data-ttu-id="2a4a8-108">既定のプロファイルの名前を検索する必要がある場合は、2番目の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="2a4a8-108">If you need to find the name of the default profile, use the second procedure.</span></span> <span data-ttu-id="2a4a8-109">セッションの現在のプロファイルの名前を検索する必要がある場合は、last プロシージャを使用します。</span><span class="sxs-lookup"><span data-stu-id="2a4a8-109">If you need to find the name of the current profile for the session, use the last procedure.</span></span> 
  
 <span data-ttu-id="2a4a8-110">**任意のプロファイルの名前を検索するには**</span><span class="sxs-lookup"><span data-stu-id="2a4a8-110">**To find the name of any profile**</span></span>
  
1. <span data-ttu-id="2a4a8-111">[MAPIAdminProfiles](mapiadminprofiles.md)を呼び出して、 **IProfAdmin**インターフェイスポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="2a4a8-111">Call [MAPIAdminProfiles](mapiadminprofiles.md) to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="2a4a8-112">プロファイルテーブルにアクセスするには、 [IProfAdmin:: getprofiletable](iprofadmin-getprofiletable.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2a4a8-112">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="2a4a8-113">プロファイルテーブルの[IMAPITable:: QueryRows](imapitable-queryrows.md)メソッドを呼び出して、テーブル内のすべての行を取得し、それぞれの行を調べてターゲットプロファイルを表しているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="2a4a8-113">Call the profile table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve all of the rows in the table and examine each one to determine if it represents your target profile.</span></span> 
    
 <span data-ttu-id="2a4a8-114">**既定のプロファイルの名前を検索するには**</span><span class="sxs-lookup"><span data-stu-id="2a4a8-114">**To find the name of the default profile**</span></span>
  
1. <span data-ttu-id="2a4a8-115">[MAPIAdminProfiles](mapiadminprofiles.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2a4a8-115">Call [MAPIAdminProfiles](mapiadminprofiles.md).</span></span>
    
2. <span data-ttu-id="2a4a8-116">プロファイルテーブルにアクセスするには、 [IProfAdmin:: getprofiletable](iprofadmin-getprofiletable.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2a4a8-116">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="2a4a8-117">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) と値が TRUE に一致する[spropertyrestriction](spropertyrestriction.md)構造を持つプロパティ制限を構築します。</span><span class="sxs-lookup"><span data-stu-id="2a4a8-117">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) with the value TRUE.</span></span>
    
4. <span data-ttu-id="2a4a8-118">[ [IMAPITable:: FindRow](imapitable-findrow.md)を呼び出して、既定のプロファイルを表すプロファイルテーブルの行を検索します。</span><span class="sxs-lookup"><span data-stu-id="2a4a8-118">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the row in the profile table that represents the default profile.</span></span> <span data-ttu-id="2a4a8-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 列には、既定のプロファイルの名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2a4a8-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column contains the name of the default profile.</span></span>
    
 <span data-ttu-id="2a4a8-120">**現在のプロファイルの名前を検索するには**</span><span class="sxs-lookup"><span data-stu-id="2a4a8-120">**To find the name of the current profile**</span></span>
  
<span data-ttu-id="2a4a8-121">現在のプロファイルの名前を検索するには、次のいずれかの手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2a4a8-121">To find the name of the current profile, complete one of the following steps:</span></span>
  
- <span data-ttu-id="2a4a8-122">現在のプロファイルのセクションの1つを表す[MAPIUID](mapiuid.md)構造体がある場合は、 _lpuid_パラメーターにそのセクションを渡して[imapisession:: openprofile](imapisession-openprofilesection.md)のセクションに渡します。</span><span class="sxs-lookup"><span data-stu-id="2a4a8-122">Assuming that you have the [MAPIUID](mapiuid.md) structure representing one of the current profile's sections, pass it in the  _lpUID_ parameter to [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md).</span></span> <span data-ttu-id="2a4a8-123">[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを使用して、プロファイルセクションの**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="2a4a8-123">Retrieve the profile section's **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property using its [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
    
- <span data-ttu-id="2a4a8-124">呼び出し[imapisession:: getstatustable](imapisession-getstatustable.md)は状態テーブルにアクセスして、その**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) 列が MAPI_SUBSYSTEM に設定されている行を検索します。</span><span class="sxs-lookup"><span data-stu-id="2a4a8-124">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table and find the row that has its **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column set to MAPI_SUBSYSTEM.</span></span> <span data-ttu-id="2a4a8-125">この行の**PR_DISPLAY_NAME**列はプロファイル名です。</span><span class="sxs-lookup"><span data-stu-id="2a4a8-125">The **PR_DISPLAY_NAME** column for this row is the profile name.</span></span> <span data-ttu-id="2a4a8-126">起動時に状態テーブルを使用しないでください。これは、MAPI スプーラーがすべてのトランスポートプロバイダーの初期化を終了するまでアプリケーションをブロックするためです。</span><span class="sxs-lookup"><span data-stu-id="2a4a8-126">Do not use the status table during start up because it blocks an application until the MAPI spooler has finished initializing all of the transport providers.</span></span> <span data-ttu-id="2a4a8-127">これにより、パフォーマンスが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2a4a8-127">This can degrade your performance.</span></span> 
    

