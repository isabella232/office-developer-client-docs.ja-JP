---
title: カスタムコードを使用してプロファイルを作成する
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
# <a name="creating-a-profile-by-using-custom-code"></a><span data-ttu-id="b5f8c-103">カスタムコードを使用してプロファイルを作成する</span><span class="sxs-lookup"><span data-stu-id="b5f8c-103">Creating a Profile by Using Custom Code</span></span>

  
  
<span data-ttu-id="b5f8c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5f8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5f8c-105">プロファイルを作成するコードの記述を選択する場合は、プロファイルエントリの順序付け方法と、各エントリに必要な情報の種類と量を理解していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b5f8c-105">If you choose to write code to create a profile, make sure that you understand how to order profile entries and the type and amount of information that is needed for each entry.</span></span> <span data-ttu-id="b5f8c-106">プロファイル内のエントリの順序付けの影響については、「 [MAPI プロファイル](mapi-profiles.md)」で説明されています。</span><span class="sxs-lookup"><span data-stu-id="b5f8c-106">The implications of ordering entries in a profile is explained in [MAPI Profiles](mapi-profiles.md).</span></span>
  
 <span data-ttu-id="b5f8c-107">**C または C++ コードでプロファイルを作成するには**</span><span class="sxs-lookup"><span data-stu-id="b5f8c-107">**To create a profile with C or C++ code**</span></span>
  
1. <span data-ttu-id="b5f8c-108">各メッセージサービスのヘッダーファイルを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="b5f8c-108">Read the header file for each message service.</span></span> <span data-ttu-id="b5f8c-109">構成する必要があるプロパティと、使用する値について説明します。</span><span class="sxs-lookup"><span data-stu-id="b5f8c-109">Understand what properties you will need to configure and what values you will use.</span></span>
    
2. <span data-ttu-id="b5f8c-110">[MAPIAdminProfiles](mapiadminprofiles.md)関数を呼び出して、 **IProfAdmin**インターフェイスポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="b5f8c-110">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
3. <span data-ttu-id="b5f8c-111">[IProfAdmin:: createprofile](iprofadmin-createprofile.md)を呼び出して、プロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="b5f8c-111">Call [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) to create your profile.</span></span> <span data-ttu-id="b5f8c-112">mapisvc.inf の **[Default services]** セクションに表示されているメッセージサービスを使用してプロファイルを作成する場合。INF ファイルで、MAPI_DEFAULT_SERVICE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="b5f8c-112">If you want to create a profile with the message services listed in the **[Default Services]** section of the MAPISVC.INF file, set the MAPI_DEFAULT_SERVICE flag.</span></span> <span data-ttu-id="b5f8c-113">ユーザーが構成情報を入力できるようにするには、MAPI_DIALOG フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="b5f8c-113">If you want to enable the user to enter configuration information, set the MAPI_DIALOG flag.</span></span> <span data-ttu-id="b5f8c-114">mapisvc.inf で必要な情報をすべて利用できない場合は、このフラグが設定されていることを確認してください。INF ファイル</span><span class="sxs-lookup"><span data-stu-id="b5f8c-114">Make sure that you set this flag if not all of the necessary information is available through the MAPISVC.INF file.</span></span> <span data-ttu-id="b5f8c-115">**createprofile**は、MSG_SERVICE_CREATE が_ulcontext_パラメーターとして設定されているプロファイルに、各メッセージサービスのエントリポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b5f8c-115">**CreateProfile** calls the entry point function for each message service to be added to the profile with MSG_SERVICE_CREATE set as the  _ulContext_ parameter.</span></span> 
    
4. <span data-ttu-id="b5f8c-116">[IProfAdmin:: adminservices](iprofadmin-adminservices.md)を呼び出して、メッセージサービス管理オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="b5f8c-116">Call [IProfAdmin::AdminServices](iprofadmin-adminservices.md) to obtain a message service administration object.</span></span> 
    
5. <span data-ttu-id="b5f8c-117">メッセージサービスの管理オブジェクトを使用して、メッセージサービスをプロファイルに追加します。</span><span class="sxs-lookup"><span data-stu-id="b5f8c-117">Use the message service administration object to add message services to the profile.</span></span> <span data-ttu-id="b5f8c-118">追加するメッセージサービスごとに、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="b5f8c-118">For each message service that you want to add:</span></span>
    
1. <span data-ttu-id="b5f8c-119">[IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md)メソッドを呼び出して、新しいメッセージサービスを作成します。</span><span class="sxs-lookup"><span data-stu-id="b5f8c-119">Call the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method to create the new message service.</span></span> 
    
2. <span data-ttu-id="b5f8c-120">[IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)を呼び出して、作成したばかりのサービスの**MAPIUID**構造と、構成プロパティを持つプロパティ値配列を渡します。</span><span class="sxs-lookup"><span data-stu-id="b5f8c-120">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), passing the **MAPIUID** structure of the service you just created and a property value array with its configuration properties.</span></span> 
    
6. <span data-ttu-id="b5f8c-121">新しく追加されたサービスの識別子 ( **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) プロパティ) を取得するには、 [IMsgServiceAdmin:: getmsgservicetable](imsgserviceadmin-getmsgservicetable.md)を呼び出してメッセージサービステーブルにアクセスし、次の行を表す行を検索します。メッセージサービス。</span><span class="sxs-lookup"><span data-stu-id="b5f8c-121">To retrieve the identifier of a newly added service, which is its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property, call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to access the message service table and search for the row that represents the message service.</span></span> <span data-ttu-id="b5f8c-122">表の最後の行は、最近追加されたメッセージサービスを表します。</span><span class="sxs-lookup"><span data-stu-id="b5f8c-122">The last row in the table will represent the most recently added message service.</span></span> 
    
<span data-ttu-id="b5f8c-123">新しいプロファイル一時を作成するには、ログオンした直後に[IProfAdmin::D eleteprofile](iprofadmin-deleteprofile.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b5f8c-123">To make a new profile temporary, call the [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md) method immediately after you log on.</span></span> <span data-ttu-id="b5f8c-124">**deleteprofile**は、新しいプロファイルを削除済みとしてマークし、セッションの間は使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="b5f8c-124">**DeleteProfile** will mark the new profile as deleted while making it usable for the duration of the session.</span></span> <span data-ttu-id="b5f8c-125">これはセッションのプロファイルテーブルに含まれないため、他のクライアントはそれを使用できません。</span><span class="sxs-lookup"><span data-stu-id="b5f8c-125">Because it will not be included in the session's profile table, other clients will be unable to use it.</span></span> 
  

