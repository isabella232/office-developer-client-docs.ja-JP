---
title: カスタム コードを使用してプロファイルを作成します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5632cd25-58f5-4b9c-906c-cd377abc3daf
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 74869293215b86c69ab4e0b1337be6014419fa3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799865"
---
# <a name="creating-a-profile-by-using-custom-code"></a><span data-ttu-id="900f3-103">カスタム コードを使用してプロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="900f3-103">Creating a Profile by Using Custom Code</span></span>

  
  
<span data-ttu-id="900f3-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="900f3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="900f3-105">プロファイルを作成するコードを記述することを選択する場合は、プロファイル エントリの種類と各エントリのために必要な情報の量を注文する方法を理解することを確認します。</span><span class="sxs-lookup"><span data-stu-id="900f3-105">If you choose to write code to create a profile, make sure that you understand how to order profile entries and the type and amount of information that is needed for each entry.</span></span> <span data-ttu-id="900f3-106">プロファイル内のエントリの順序の影響は、 [MAPI プロファイル](mapi-profiles.md)で説明しています。</span><span class="sxs-lookup"><span data-stu-id="900f3-106">The implications of ordering entries in a profile is explained in [MAPI Profiles](mapi-profiles.md).</span></span>
  
 <span data-ttu-id="900f3-107">**C または C++ のコードでプロファイルを作成するには**</span><span class="sxs-lookup"><span data-stu-id="900f3-107">**To create a profile with C or C++ code**</span></span>
  
1. <span data-ttu-id="900f3-108">各メッセージ サービス用のヘッダー ファイルを参照します。</span><span class="sxs-lookup"><span data-stu-id="900f3-108">Read the header file for each message service.</span></span> <span data-ttu-id="900f3-109">構成する必要がどのようなプロパティを理解し、使用しました。</span><span class="sxs-lookup"><span data-stu-id="900f3-109">Understand what properties you will need to configure and what values you will use.</span></span>
    
2. <span data-ttu-id="900f3-110">**IProfAdmin**インターフェイス ポインターを取得するために[MAPIAdminProfiles](mapiadminprofiles.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="900f3-110">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
3. <span data-ttu-id="900f3-111">プロファイルを作成するのには[IProfAdmin::CreateProfile](iprofadmin-createprofile.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="900f3-111">Call [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) to create your profile.</span></span> <span data-ttu-id="900f3-112">場合、MAPISVC の **[サービスの既定値]** セクションに記載されているメッセージ サービスを使用してプロファイルを作成します。INF ファイルは、MAPI_DEFAULT_SERVICE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="900f3-112">If you want to create a profile with the message services listed in the **[Default Services]** section of the MAPISVC.INF file, set the MAPI_DEFAULT_SERVICE flag.</span></span> <span data-ttu-id="900f3-113">構成情報を入力するユーザーを有効にする場合は、MAPI_DIALOG フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="900f3-113">If you want to enable the user to enter configuration information, set the MAPI_DIALOG flag.</span></span> <span data-ttu-id="900f3-114">このフラグを設定するかどうかすべての必要な情報は、MAPISVC で利用できるようにしてください。INF ファイルです。</span><span class="sxs-lookup"><span data-stu-id="900f3-114">Make sure that you set this flag if not all of the necessary information is available through the MAPISVC.INF file.</span></span> <span data-ttu-id="900f3-115">**CreateProfile**は、MSG_SERVICE_CREATE の_ulContext_のパラメーターとして設定すると、プロファイルに追加するには、各メッセージ サービスのエントリ ポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="900f3-115">**CreateProfile** calls the entry point function for each message service to be added to the profile with MSG_SERVICE_CREATE set as the  _ulContext_ parameter.</span></span> 
    
4. <span data-ttu-id="900f3-116">メッセージ サービス管理オブジェクトを取得する[IProfAdmin::AdminServices](iprofadmin-adminservices.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="900f3-116">Call [IProfAdmin::AdminServices](iprofadmin-adminservices.md) to obtain a message service administration object.</span></span> 
    
5. <span data-ttu-id="900f3-117">メッセージ サービスをプロファイルに追加するのにには、メッセージ サービスの管理オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="900f3-117">Use the message service administration object to add message services to the profile.</span></span> <span data-ttu-id="900f3-118">メッセージ サービスごとに追加します。</span><span class="sxs-lookup"><span data-stu-id="900f3-118">For each message service that you want to add:</span></span>
    
1. <span data-ttu-id="900f3-119">新しいメッセージ サービスを作成する[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="900f3-119">Call the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method to create the new message service.</span></span> 
    
2. <span data-ttu-id="900f3-120">[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)、作成したサービスの**MAPIUID**構造体とその構成のプロパティを持つプロパティ値の配列を渡すことを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="900f3-120">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), passing the **MAPIUID** structure of the service you just created and a property value array with its configuration properties.</span></span> 
    
6. <span data-ttu-id="900f3-121">その**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) プロパティでは、新しく追加されたサービスの識別子を取得するために、メッセージ サービス テーブルを表す行の検索にアクセスする[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)を呼び出すメッセージ サービスです。</span><span class="sxs-lookup"><span data-stu-id="900f3-121">To retrieve the identifier of a newly added service, which is its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property, call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to access the message service table and search for the row that represents the message service.</span></span> <span data-ttu-id="900f3-122">テーブルの最後の行は、最後に追加されたメッセージ サービスを表します。</span><span class="sxs-lookup"><span data-stu-id="900f3-122">The last row in the table will represent the most recently added message service.</span></span> 
    
<span data-ttu-id="900f3-123">新しいプロファイルは、一時的なものには、ログオンした後にすぐに[IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="900f3-123">To make a new profile temporary, call the [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md) method immediately after you log on.</span></span> <span data-ttu-id="900f3-124">**DeleteProfile**は、セッション中に使用するときに削除されると、新しいプロファイルをマークします。</span><span class="sxs-lookup"><span data-stu-id="900f3-124">**DeleteProfile** will mark the new profile as deleted while making it usable for the duration of the session.</span></span> <span data-ttu-id="900f3-125">していないため、セッションのプロファイル テーブルに、に他のクライアントはそれを使用することができません。</span><span class="sxs-lookup"><span data-stu-id="900f3-125">Because it will not be included in the session's profile table, other clients will be unable to use it.</span></span> 
  

