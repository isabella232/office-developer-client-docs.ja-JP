---
title: カスタム コードを使用したプロファイルの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5632cd25-58f5-4b9c-906c-cd377abc3daf
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f3270528194b3cc3429d3afec153355349dabbff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413305"
---
# <a name="creating-a-profile-by-using-custom-code"></a><span data-ttu-id="10d6e-103">カスタム コードを使用したプロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="10d6e-103">Creating a Profile by Using Custom Code</span></span>

  
  
<span data-ttu-id="10d6e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10d6e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10d6e-105">プロファイルを作成するコードを作成する場合は、プロファイル エントリの注文方法と、各エントリに必要な情報の種類と量を理解してください。</span><span class="sxs-lookup"><span data-stu-id="10d6e-105">If you choose to write code to create a profile, make sure that you understand how to order profile entries and the type and amount of information that is needed for each entry.</span></span> <span data-ttu-id="10d6e-106">プロファイル内のエントリを順序付けする場合の影響については [、「MAPI プロファイル」で説明します](mapi-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="10d6e-106">The implications of ordering entries in a profile is explained in [MAPI Profiles](mapi-profiles.md).</span></span>
  
 <span data-ttu-id="10d6e-107">**C または C++ コードを使用してプロファイルを作成するには**</span><span class="sxs-lookup"><span data-stu-id="10d6e-107">**To create a profile with C or C++ code**</span></span>
  
1. <span data-ttu-id="10d6e-108">各メッセージ サービスのヘッダー ファイルを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="10d6e-108">Read the header file for each message service.</span></span> <span data-ttu-id="10d6e-109">構成する必要があるプロパティと、使用する値を理解します。</span><span class="sxs-lookup"><span data-stu-id="10d6e-109">Understand what properties you will need to configure and what values you will use.</span></span>
    
2. <span data-ttu-id="10d6e-110">[MAPIAdminProfiles 関数を呼び出](mapiadminprofiles.md)して **、IProfAdmin** インターフェイス ポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="10d6e-110">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
3. <span data-ttu-id="10d6e-111">[IProfAdmin::CreateProfile](iprofadmin-createprofile.md)を呼び出してプロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="10d6e-111">Call [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) to create your profile.</span></span> <span data-ttu-id="10d6e-112">MAPISVC の [既定のサービス] セクションに一覧表示されているメッセージ サービスを使用してプロファイルを作成する場合。INF ファイルで、フラグを設定MAPI_DEFAULT_SERVICEします。</span><span class="sxs-lookup"><span data-stu-id="10d6e-112">If you want to create a profile with the message services listed in the **[Default Services]** section of the MAPISVC.INF file, set the MAPI_DEFAULT_SERVICE flag.</span></span> <span data-ttu-id="10d6e-113">ユーザーが構成情報を入力する場合は、このフラグをMAPI_DIALOGします。</span><span class="sxs-lookup"><span data-stu-id="10d6e-113">If you want to enable the user to enter configuration information, set the MAPI_DIALOG flag.</span></span> <span data-ttu-id="10d6e-114">MAPISVC を介して必要な情報の一部が利用できない場合は、必ずこのフラグを設定してください。INF ファイル。</span><span class="sxs-lookup"><span data-stu-id="10d6e-114">Make sure that you set this flag if not all of the necessary information is available through the MAPISVC.INF file.</span></span> <span data-ttu-id="10d6e-115">**CreateProfile は** 、メッセージ サービスごとにエントリ ポイント関数を呼び出し  _、ulContext_ パラメーターとしてMSG_SERVICE_CREATEプロファイルに追加します。</span><span class="sxs-lookup"><span data-stu-id="10d6e-115">**CreateProfile** calls the entry point function for each message service to be added to the profile with MSG_SERVICE_CREATE set as the  _ulContext_ parameter.</span></span> 
    
4. <span data-ttu-id="10d6e-116">[IProfAdmin::AdminServices を呼び出](iprofadmin-adminservices.md)して、メッセージ サービス管理オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="10d6e-116">Call [IProfAdmin::AdminServices](iprofadmin-adminservices.md) to obtain a message service administration object.</span></span> 
    
5. <span data-ttu-id="10d6e-117">メッセージ サービス管理オブジェクトを使用して、メッセージ サービスをプロファイルに追加します。</span><span class="sxs-lookup"><span data-stu-id="10d6e-117">Use the message service administration object to add message services to the profile.</span></span> <span data-ttu-id="10d6e-118">追加するメッセージ サービスごとに、次の処理を行います。</span><span class="sxs-lookup"><span data-stu-id="10d6e-118">For each message service that you want to add:</span></span>
    
1. <span data-ttu-id="10d6e-119">新しい [メッセージ サービスを作成するには、IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="10d6e-119">Call the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method to create the new message service.</span></span> 
    
2. <span data-ttu-id="10d6e-120">[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)を呼び出し、作成したサービスの **MAPIUID** 構造と、その構成プロパティを持つプロパティ値配列を渡します。</span><span class="sxs-lookup"><span data-stu-id="10d6e-120">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), passing the **MAPIUID** structure of the service you just created and a property value array with its configuration properties.</span></span> 
    
6. <span data-ttu-id="10d6e-121">PR_SERVICE_UID ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) プロパティである新しく追加されたサービスの識別子を取得するには[、IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)を呼び出してメッセージ サービス テーブルにアクセスし、メッセージ サービスを表す行を検索します。 </span><span class="sxs-lookup"><span data-stu-id="10d6e-121">To retrieve the identifier of a newly added service, which is its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property, call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to access the message service table and search for the row that represents the message service.</span></span> <span data-ttu-id="10d6e-122">表の最後の行は、最近追加されたメッセージ サービスを表します。</span><span class="sxs-lookup"><span data-stu-id="10d6e-122">The last row in the table will represent the most recently added message service.</span></span> 
    
<span data-ttu-id="10d6e-123">新しいプロファイルを一時的に作成するには、ログオン直後に [IProfAdmin::D eleteProfile](iprofadmin-deleteprofile.md) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="10d6e-123">To make a new profile temporary, call the [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md) method immediately after you log on.</span></span> <span data-ttu-id="10d6e-124">**DeleteProfile は** 、新しいプロファイルを削除済みとしてマークし、セッションの期間中は使用できます。</span><span class="sxs-lookup"><span data-stu-id="10d6e-124">**DeleteProfile** will mark the new profile as deleted while making it usable for the duration of the session.</span></span> <span data-ttu-id="10d6e-125">セッションのプロファイル テーブルには含まれませんので、他のクライアントでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="10d6e-125">Because it will not be included in the session's profile table, other clients will be unable to use it.</span></span> 
  

