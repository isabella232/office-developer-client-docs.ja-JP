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
# <a name="finding-a-profile-name"></a><span data-ttu-id="c1c21-103">プロファイル名の検索</span><span class="sxs-lookup"><span data-stu-id="c1c21-103">Finding a Profile Name</span></span>

  
  
<span data-ttu-id="c1c21-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1c21-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1c21-105">クライアントは、セッションに現在使用されているプロファイルの名前、既定のプロファイルの名前、またはコンピューターにインストールされている代替プロファイルの名前を見つける必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="c1c21-105">Clients sometimes need to find the name of the profile currently being used for the session, the name of the default profile, or the name of an alternate profile installed on the computer.</span></span>
  
<span data-ttu-id="c1c21-106">セッション中にプロファイルの名前を取得するには、いくつかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="c1c21-106">There are a few ways to retrieve the name of a profile during the course of a session.</span></span> <span data-ttu-id="c1c21-107">セッションで必ずしも使用されていないプロファイルの名前を見つける必要がある場合は、最初の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="c1c21-107">If you need to find the name of a profile that is not necessarily the one being used for the session, use the first procedure.</span></span> <span data-ttu-id="c1c21-108">既定のプロファイルの名前を見つける必要がある場合は、2 番目の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="c1c21-108">If you need to find the name of the default profile, use the second procedure.</span></span> <span data-ttu-id="c1c21-109">セッションの現在のプロファイルの名前を見つける必要がある場合は、最後の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="c1c21-109">If you need to find the name of the current profile for the session, use the last procedure.</span></span> 
  
 <span data-ttu-id="c1c21-110">**プロファイルの名前を見つけるには**</span><span class="sxs-lookup"><span data-stu-id="c1c21-110">**To find the name of any profile**</span></span>
  
1. <span data-ttu-id="c1c21-111">[MAPIAdminProfiles を呼び出](mapiadminprofiles.md)して **、IProfAdmin インターフェイス ポインターを** 取得します。</span><span class="sxs-lookup"><span data-stu-id="c1c21-111">Call [MAPIAdminProfiles](mapiadminprofiles.md) to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="c1c21-112">[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)を呼び出して、プロファイル テーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="c1c21-112">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="c1c21-113">プロファイル テーブルの [IMAPITable::QueryRows](imapitable-queryrows.md) メソッドを呼び出して、テーブル内のすべての行を取得し、各行を調べて、ターゲット プロファイルを表すかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="c1c21-113">Call the profile table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve all of the rows in the table and examine each one to determine if it represents your target profile.</span></span> 
    
 <span data-ttu-id="c1c21-114">**既定のプロファイルの名前を見つけるには**</span><span class="sxs-lookup"><span data-stu-id="c1c21-114">**To find the name of the default profile**</span></span>
  
1. <span data-ttu-id="c1c21-115">[MAPIAdminProfiles を呼び出します](mapiadminprofiles.md)。</span><span class="sxs-lookup"><span data-stu-id="c1c21-115">Call [MAPIAdminProfiles](mapiadminprofiles.md).</span></span>
    
2. <span data-ttu-id="c1c21-116">[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)を呼び出して、プロファイル テーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="c1c21-116">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="c1c21-117">[SPropertyRestriction](spropertyrestriction.md)構造体を使用してプロパティ制限を構築し、PR_DEFAULT_PROFILE **(** [PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) と値 TRUE を一致します。</span><span class="sxs-lookup"><span data-stu-id="c1c21-117">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) with the value TRUE.</span></span>
    
4. <span data-ttu-id="c1c21-118">[IMAPITable::FindRow を](imapitable-findrow.md)呼び出して、既定のプロファイルを表すプロファイル テーブル内の行を検索します。</span><span class="sxs-lookup"><span data-stu-id="c1c21-118">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the row in the profile table that represents the default profile.</span></span> <span data-ttu-id="c1c21-119">**[PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)列には、既定のプロファイルの名前が含まれる。</span><span class="sxs-lookup"><span data-stu-id="c1c21-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column contains the name of the default profile.</span></span>
    
 <span data-ttu-id="c1c21-120">**現在のプロファイルの名前を見つけるには**</span><span class="sxs-lookup"><span data-stu-id="c1c21-120">**To find the name of the current profile**</span></span>
  
<span data-ttu-id="c1c21-121">現在のプロファイルの名前を見つけるには、次のいずれかの手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c1c21-121">To find the name of the current profile, complete one of the following steps:</span></span>
  
- <span data-ttu-id="c1c21-122">現在のプロファイルのセクションの 1 つを表す [MAPIUID](mapiuid.md) 構造がある場合は  _、lpUID_ パラメーターで [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)に渡します。</span><span class="sxs-lookup"><span data-stu-id="c1c21-122">Assuming that you have the [MAPIUID](mapiuid.md) structure representing one of the current profile's sections, pass it in the  _lpUID_ parameter to [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md).</span></span> <span data-ttu-id="c1c21-123">IMAPIProp::GetProps メソッドを **PR_PROFILE_NAME** プロファイル セクションのプロパティ [(PidTagProfileName)](pidtagprofilename-canonical-property.md)[プロパティを取得](imapiprop-getprops.md)します。</span><span class="sxs-lookup"><span data-stu-id="c1c21-123">Retrieve the profile section's **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property using its [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
    
- <span data-ttu-id="c1c21-124">[IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出して、状態テーブルにアクセスし **、PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) 列が MAPI_SUBSYSTEM に設定されている行を検索します。</span><span class="sxs-lookup"><span data-stu-id="c1c21-124">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table and find the row that has its **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column set to MAPI_SUBSYSTEM.</span></span> <span data-ttu-id="c1c21-125">この **PR_DISPLAY_NAME** の列はプロファイル名です。</span><span class="sxs-lookup"><span data-stu-id="c1c21-125">The **PR_DISPLAY_NAME** column for this row is the profile name.</span></span> <span data-ttu-id="c1c21-126">MAPI スプーラーがすべてのトランスポート プロバイダーの初期化を完了するまで、アプリケーションをブロックするために、起動中に状態テーブルを使用しない。</span><span class="sxs-lookup"><span data-stu-id="c1c21-126">Do not use the status table during start up because it blocks an application until the MAPI spooler has finished initializing all of the transport providers.</span></span> <span data-ttu-id="c1c21-127">これにより、パフォーマンスが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c1c21-127">This can degrade your performance.</span></span> 
    

