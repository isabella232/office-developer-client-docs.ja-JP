---
title: MAPI の追加について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 78e2806d-bb6f-cd96-21f1-b7c667c73c33
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fefa77a15cc2b8c72a41b29e6299f159a893cee8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322163"
---
# <a name="about-mapi-additions"></a><span data-ttu-id="460fe-103">MAPI の追加について</span><span class="sxs-lookup"><span data-stu-id="460fe-103">About MAPI additions</span></span>

<span data-ttu-id="460fe-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="460fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="460fe-105">mapi 追加機能は、メッセージングアプリケーションプログラミングインターフェイス (mapi) に属する api (データ型、関数、プロパティなど) で、以前は公開されておらず、mapi プログラマーズリファレンスの一部として文書化されています。</span><span class="sxs-lookup"><span data-stu-id="460fe-105">MAPI additions are APIs that belong to Messaging Application Programming Interface (MAPI), such as data types, functions, and properties, that were previously not exposed and documented as part of the MAPI Programmer's Reference.</span></span> <span data-ttu-id="460fe-106">これらには、次の定義とプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="460fe-106">They include the following definitions and properties.</span></span>
  
## <a name="constant-definitions"></a><span data-ttu-id="460fe-107">定数の定義</span><span class="sxs-lookup"><span data-stu-id="460fe-107">Constant definitions</span></span>

- <span data-ttu-id="460fe-108">**[その他の MAPI 定数](mapi-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-108">**[Additional MAPI Constants](mapi-constants.md)**</span></span>
  
## <a name="data-types"></a><span data-ttu-id="460fe-109">データ型</span><span class="sxs-lookup"><span data-stu-id="460fe-109">Data types</span></span>

- <span data-ttu-id="460fe-110">**[EXCHANGE_STORE_VERSION_NUM](exchange_store_version_num.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-110">**[EXCHANGE_STORE_VERSION_NUM](exchange_store_version_num.md)**</span></span>
    
- <span data-ttu-id="460fe-111">**[FollowUpStatus](followupstatus.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-111">**[FollowUpStatus](followupstatus.md)**</span></span>
    
- <span data-ttu-id="460fe-112">**[性別](gender.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-112">**[Gender](gender.md)**</span></span>
    
- <span data-ttu-id="460fe-113">**[OlFlagIcon](olflagicon.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-113">**[OlFlagIcon](olflagicon.md)**</span></span>
    
## <a name="functions"></a><span data-ttu-id="460fe-114">関数</span><span class="sxs-lookup"><span data-stu-id="460fe-114">Functions</span></span>

- <span data-ttu-id="460fe-115">**[FixMAPI](fixmapi.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-115">**[FixMAPI](fixmapi.md)**</span></span>
    
## <a name="properties"></a><span data-ttu-id="460fe-116">プロパティ</span><span class="sxs-lookup"><span data-stu-id="460fe-116">Properties</span></span>

<span data-ttu-id="460fe-117">通常、次のプロパティは message オブジェクトで公開されます。</span><span class="sxs-lookup"><span data-stu-id="460fe-117">The following properties are generally exposed by message objects.</span></span>
  
- <span data-ttu-id="460fe-118">**[PR_BODY_W](pidtagbody-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-118">**[PR_BODY_W](pidtagbody-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-119">**[PR_CONFLICT_ITEMS](pidtagconflictitems-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-119">**[PR_CONFLICT_ITEMS](pidtagconflictitems-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-120">**[PR_DISPLAY_BCC_W](pidtagdisplaybcc-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-120">**[PR_DISPLAY_BCC_W](pidtagdisplaybcc-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-121">**[PR_DISPLAY_CC_W](pidtagdisplaycc-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-121">**[PR_DISPLAY_CC_W](pidtagdisplaycc-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-122">**[PR_DISPLAY_TO_W](pidtagdisplayto-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-122">**[PR_DISPLAY_TO_W](pidtagdisplayto-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-123">**[PR_FLAG_STATUS](pidtagflagstatus-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-123">**[PR_FLAG_STATUS](pidtagflagstatus-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-124">**[PR_FOLLOWUP_ICON](pidtagfollowupicon-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-124">**[PR_FOLLOWUP_ICON](pidtagfollowupicon-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-125">**[PR_INETMAIL_OVERRIDE_FORMAT](pidtaginternetmailoverrideformat-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-125">**[PR_INETMAIL_OVERRIDE_FORMAT](pidtaginternetmailoverrideformat-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-126">**[PR_MESSAGE_CLASS_W](pidtagmessageclass-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-126">**[PR_MESSAGE_CLASS_W](pidtagmessageclass-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-127">**[PR_MSG_EDITOR_FORMAT](pidtagmessageeditorformat-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-127">**[PR_MSG_EDITOR_FORMAT](pidtagmessageeditorformat-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-128">**[PR_NORMALIZED_SUBJECT_W](pidtagnormalizedsubject-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-128">**[PR_NORMALIZED_SUBJECT_W](pidtagnormalizedsubject-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-129">**[PR_SENDER_ADDRTYPE_W](pidtagsenderaddresstype-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-129">**[PR_SENDER_ADDRTYPE_W](pidtagsenderaddresstype-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-130">**[PR_SENDER_EMAIL_ADDRESS_W](pidtagsenderemailaddress-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-130">**[PR_SENDER_EMAIL_ADDRESS_W](pidtagsenderemailaddress-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-131">**[PR_SENDER_NAME_W](pidtagsendername-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-131">**[PR_SENDER_NAME_W](pidtagsendername-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-132">**[PR_SENT_REPRESENTING_ADDRTYPE_W](pidtagsentrepresentingaddresstype-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-132">**[PR_SENT_REPRESENTING_ADDRTYPE_W](pidtagsentrepresentingaddresstype-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-133">**[PR_SENT_REPRESENTING_EMAIL_ADDRESS_W](pidtagsentrepresentingemailaddress-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-133">**[PR_SENT_REPRESENTING_EMAIL_ADDRESS_W](pidtagsentrepresentingemailaddress-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-134">**[PR_SENT_REPRESENTING_NAME_W](pidtagsentrepresentingname-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-134">**[PR_SENT_REPRESENTING_NAME_W](pidtagsentrepresentingname-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-135">**[PR_SUBJECT_PREFIX_W](pidtagsubjectprefix-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-135">**[PR_SUBJECT_PREFIX_W](pidtagsubjectprefix-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-136">**[PR_SUBJECT_W](pidtagsubject-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-136">**[PR_SUBJECT_W](pidtagsubject-canonical-property.md)**</span></span>
    
<span data-ttu-id="460fe-137">次のプロパティは、アドレス帳の contents table オブジェクトで公開されています。</span><span class="sxs-lookup"><span data-stu-id="460fe-137">The following properties are exposed by address book contents table objects.</span></span>
  
- <span data-ttu-id="460fe-138">**[PR_DISPLAY_TYPE_EX](pidtagdisplaytypeex-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-138">**[PR_DISPLAY_TYPE_EX](pidtagdisplaytypeex-canonical-property.md)**</span></span>
    
<span data-ttu-id="460fe-139">アドレス帳のコンテナーオブジェクトでは、次のプロパティが公開されます。</span><span class="sxs-lookup"><span data-stu-id="460fe-139">The following properties are exposed by address book container objects.</span></span>
  
- <span data-ttu-id="460fe-140">**[PR_EMS_AB_SERVER](pidtagemsabserver-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-140">**[PR_EMS_AB_SERVER](pidtagemsabserver-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-141">**[PR_EMS_AB_SERVER_A](pidtagemsabserver-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-141">**[PR_EMS_AB_SERVER_A](pidtagemsabserver-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-142">**[PR_EMS_AB_SERVER_W](pidtagemsabserver-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-142">**[PR_EMS_AB_SERVER_W](pidtagemsabserver-canonical-property.md)**</span></span>
    
<span data-ttu-id="460fe-143">folder オブジェクトでは、次のプロパティが公開されます。</span><span class="sxs-lookup"><span data-stu-id="460fe-143">The following properties are exposed by folder objects.</span></span>
  
- <span data-ttu-id="460fe-144">**[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-144">**[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-145">**[PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-145">**[PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md)**</span></span>
    
<span data-ttu-id="460fe-146">次のプロパティは、メッセージングユーザーオブジェクトによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="460fe-146">The following properties are exposed by messaging user objects.</span></span>
  
- <span data-ttu-id="460fe-147">**[PR_ASSISTANT_TELEPHONE_NUMBER_W](pidtagassistanttelephonenumber-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-147">**[PR_ASSISTANT_TELEPHONE_NUMBER_W](pidtagassistanttelephonenumber-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-148">**[PR_ASSISTANT_W](pidtagassistant-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-148">**[PR_ASSISTANT_W](pidtagassistant-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-149">**[PR_ATTACHMENT_CONTACTPHOTO](pidtagattachmentcontactphoto-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-149">**[PR_ATTACHMENT_CONTACTPHOTO](pidtagattachmentcontactphoto-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-150">**[PR_BIRTHDAY](pidtagbirthday-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-150">**[PR_BIRTHDAY](pidtagbirthday-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-151">**[PR_BUSINESS_FAX_NUMBER_W](pidtagbusinessfaxnumber-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-151">**[PR_BUSINESS_FAX_NUMBER_W](pidtagbusinessfaxnumber-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-152">**[PR_BUSINESS_HOME_PAGE_W](pidtagbusinesshomepage-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-152">**[PR_BUSINESS_HOME_PAGE_W](pidtagbusinesshomepage-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-153">**[PR_CALLBACK_TELEPHONE_NUMBER_W](pidtagcallbacktelephonenumber-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-153">**[PR_CALLBACK_TELEPHONE_NUMBER_W](pidtagcallbacktelephonenumber-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-154">**[PR_CAR_TELEPHONE_NUMBER_W](pidtagcartelephonenumber-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-154">**[PR_CAR_TELEPHONE_NUMBER_W](pidtagcartelephonenumber-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-155">**[PR_CELLULAR_TELEPHONE_NUMBER_W](pidtagmobiletelephonenumber-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-155">**[PR_CELLULAR_TELEPHONE_NUMBER_W](pidtagmobiletelephonenumber-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-156">**[PR_CHILDRENS_NAMES_W](pidtagchildrensnames-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-156">**[PR_CHILDRENS_NAMES_W](pidtagchildrensnames-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-157">**[PR_DEPARTMENT_NAME_W](pidtagdepartmentname-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-157">**[PR_DEPARTMENT_NAME_W](pidtagdepartmentname-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-158">**[PR_DISPLAY_NAME_PREFIX_W](pidtagdisplaynameprefix-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-158">**[PR_DISPLAY_NAME_PREFIX_W](pidtagdisplaynameprefix-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-159">**[PR_GENDER](pidtaggender-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-159">**[PR_GENDER](pidtaggender-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-160">**[PR_GENERATION_W](pidtaggeneration-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-160">**[PR_GENERATION_W](pidtaggeneration-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-161">**[PR_GIVEN_NAME_W](pidtaggivenname-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-161">**[PR_GIVEN_NAME_W](pidtaggivenname-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-162">**[PR_HOBBIES_W](pidtaghobbies-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-162">**[PR_HOBBIES_W](pidtaghobbies-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-163">**[PR_HOME_ADDRESS_CITY_W](pidtaghomeaddresscity-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-163">**[PR_HOME_ADDRESS_CITY_W](pidtaghomeaddresscity-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-164">**[PR_HOME_ADDRESS_COUNTRY_W](pidtaghomeaddresscountry-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-164">**[PR_HOME_ADDRESS_COUNTRY_W](pidtaghomeaddresscountry-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-165">**[PR_HOME_ADDRESS_POST_OFFICE_BOX_W](pidtaghomeaddresspostofficebox-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-165">**[PR_HOME_ADDRESS_POST_OFFICE_BOX_W](pidtaghomeaddresspostofficebox-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-166">**[PR_HOME_ADDRESS_POSTAL_CODE_W](pidtaghomeaddresspostalcode-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-166">**[PR_HOME_ADDRESS_POSTAL_CODE_W](pidtaghomeaddresspostalcode-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-167">**[PR_HOME_ADDRESS_STATE_OR_PROVINCE_W](pidtaghomeaddressstateorprovince-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-167">**[PR_HOME_ADDRESS_STATE_OR_PROVINCE_W](pidtaghomeaddressstateorprovince-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-168">**[PR_HOME_ADDRESS_STREET_W](pidtaghomeaddressstreet-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-168">**[PR_HOME_ADDRESS_STREET_W](pidtaghomeaddressstreet-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-169">**[PR_HOME_FAX_NUMBER_W](pidtaghomefaxnumber-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-169">**[PR_HOME_FAX_NUMBER_W](pidtaghomefaxnumber-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-170">**[PR_HOME_TELEPHONE_NUMBER_W](pidtaghometelephonenumber-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-170">**[PR_HOME_TELEPHONE_NUMBER_W](pidtaghometelephonenumber-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-171">**[PR_KEYWORD_W](pidtagkeyword-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-171">**[PR_KEYWORD_W](pidtagkeyword-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-172">**[PR_MANAGER_NAME_W](pidtagmanagername-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-172">**[PR_MANAGER_NAME_W](pidtagmanagername-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-173">**[PR_MIDDLE_NAME_W](pidtagmiddlename-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-173">**[PR_MIDDLE_NAME_W](pidtagmiddlename-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-174">**[PR_NICKNAME_W](pidtagnickname-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-174">**[PR_NICKNAME_W](pidtagnickname-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-175">**[PR_OFFICE_LOCATION_W](pidtagofficelocation-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-175">**[PR_OFFICE_LOCATION_W](pidtagofficelocation-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-176">**[PR_OFFICE_TELEPHONE_NUMBER_W](pidtagbusinesstelephonenumber-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-176">**[PR_OFFICE_TELEPHONE_NUMBER_W](pidtagbusinesstelephonenumber-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-177">**[PR_OTHER_ADDRESS_CITY_W](pidtagotheraddresscity-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-177">**[PR_OTHER_ADDRESS_CITY_W](pidtagotheraddresscity-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-178">**[PR_OTHER_ADDRESS_COUNTRY_W](pidtagotheraddresscountry-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-178">**[PR_OTHER_ADDRESS_COUNTRY_W](pidtagotheraddresscountry-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-179">**[PR_OTHER_ADDRESS_POST_OFFICE_BOX_W](pidtagotheraddresspostofficebox-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-179">**[PR_OTHER_ADDRESS_POST_OFFICE_BOX_W](pidtagotheraddresspostofficebox-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-180">**[PR_OTHER_ADDRESS_POSTAL_CODE_W](pidtagotheraddresspostalcode-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-180">**[PR_OTHER_ADDRESS_POSTAL_CODE_W](pidtagotheraddresspostalcode-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-181">**[PR_OTHER_ADDRESS_STATE_OR_PROVINCE_W](pidtagotheraddressstateorprovince-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-181">**[PR_OTHER_ADDRESS_STATE_OR_PROVINCE_W](pidtagotheraddressstateorprovince-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-182">**[PR_OTHER_ADDRESS_STREET_W](pidtagotheraddressstreet-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-182">**[PR_OTHER_ADDRESS_STREET_W](pidtagotheraddressstreet-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-183">**[PR_PAGER_TELEPHONE_NUMBER_W](pidtagpagertelephonenumber-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-183">**[PR_PAGER_TELEPHONE_NUMBER_W](pidtagpagertelephonenumber-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-184">**[PR_PERSONAL_HOME_PAGE_W](pidtagpersonalhomepage-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-184">**[PR_PERSONAL_HOME_PAGE_W](pidtagpersonalhomepage-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-185">**[PR_PRIMARY_TELEPHONE_NUMBER_W](pidtagprimarytelephonenumber-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-185">**[PR_PRIMARY_TELEPHONE_NUMBER_W](pidtagprimarytelephonenumber-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-186">**[PR_PROFESSION_W](pidtagprofession-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-186">**[PR_PROFESSION_W](pidtagprofession-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-187">**[PR_SPOUSE_NAME_W](pidtagspousename-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-187">**[PR_SPOUSE_NAME_W](pidtagspousename-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-188">**[PR_SURNAME_W](pidtagsurname-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-188">**[PR_SURNAME_W](pidtagsurname-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-189">**[PR_TITLE_W](pidtagtitle-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-189">**[PR_TITLE_W](pidtagtitle-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-190">**[PR_TTYTDD_PHONE_NUMBER_W](pidtagttytddphonenumber-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-190">**[PR_TTYTDD_PHONE_NUMBER_W](pidtagttytddphonenumber-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-191">**[PR_WEDDING_ANNIVERSARY](pidtagweddinganniversary-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-191">**[PR_WEDDING_ANNIVERSARY](pidtagweddinganniversary-canonical-property.md)**</span></span>
    
<span data-ttu-id="460fe-192">次のプロパティは、プロファイルセクションオブジェクトによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="460fe-192">The following properties are exposed by profile section objects.</span></span>
  
- <span data-ttu-id="460fe-193">**[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-193">**[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-194">**[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-194">**[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-195">**[PR_PROVIDER_DISPLAY_NAME_W](pidtagproviderdisplayname-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-195">**[PR_PROVIDER_DISPLAY_NAME_W](pidtagproviderdisplayname-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-196">**[PR_PROVIDER_ICON_W](pidtagprovidericon-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-196">**[PR_PROVIDER_ICON_W](pidtagprovidericon-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-197">**[PR_ROH_FLAGS](pidtagrpcoverhttpflags-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-197">**[PR_ROH_FLAGS](pidtagrpcoverhttpflags-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-198">**[PR_ROH_PROXY_AUTH_SCHEME](pidtagrpcoverhttpproxyauthscheme-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-198">**[PR_ROH_PROXY_AUTH_SCHEME](pidtagrpcoverhttpproxyauthscheme-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-199">**[PR_ROH_PROXY_PRINCIPAL_NAME](pidtagrpcoverhttpproxyprincipalname-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-199">**[PR_ROH_PROXY_PRINCIPAL_NAME](pidtagrpcoverhttpproxyprincipalname-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-200">**[PR_ROH_PROXY_SERVER](pidtagrpcoverhttpproxyserver-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-200">**[PR_ROH_PROXY_SERVER](pidtagrpcoverhttpproxyserver-canonical-property.md)**</span></span>
    
<span data-ttu-id="460fe-201">store オブジェクトでは、次のプロパティが公開されます。</span><span class="sxs-lookup"><span data-stu-id="460fe-201">The following properties are exposed by store objects.</span></span>
  
- <span data-ttu-id="460fe-202">**[PR_IPM_APPOINTMENT_ENTRYID](pidtagipmappointmententryid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-202">**[PR_IPM_APPOINTMENT_ENTRYID](pidtagipmappointmententryid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-203">**[PR_IPM_CONTACT_ENTRYID](pidtagipmcontactentryid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-203">**[PR_IPM_CONTACT_ENTRYID](pidtagipmcontactentryid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-204">**[PR_IPM_DRAFTS_ENTRYID](pidtagipmdraftsentryid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-204">**[PR_IPM_DRAFTS_ENTRYID](pidtagipmdraftsentryid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-205">**[PR_IPM_JOURNAL_ENTRYID](pidtagipmjournalentryid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-205">**[PR_IPM_JOURNAL_ENTRYID](pidtagipmjournalentryid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-206">**[PR_IPM_NOTE_ENTRYID](pidtagipmnoteentryid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-206">**[PR_IPM_NOTE_ENTRYID](pidtagipmnoteentryid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-207">**[PR_IPM_TASK_ENTRYID](pidtagipmtaskentryid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-207">**[PR_IPM_TASK_ENTRYID](pidtagipmtaskentryid-canonical-property.md)**</span></span>
    
<span data-ttu-id="460fe-208">次のプロパティは、ストアオブジェクトによって公開され、ストア上の電子メールの特定の要素を検索するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="460fe-208">The following properties are exposed by store objects and are used in searching specific elements of an email on the store.</span></span>
  
- <span data-ttu-id="460fe-209">**[PR_SEARCH_ATTACHMENTS_W](pidtagsearchattachments-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-209">**[PR_SEARCH_ATTACHMENTS_W](pidtagsearchattachments-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-210">**[PR_SEARCH_RECIP_EMAIL_BCC_W](pidtagsearchrecipientemailbcc-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-210">**[PR_SEARCH_RECIP_EMAIL_BCC_W](pidtagsearchrecipientemailbcc-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-211">**[PR_SEARCH_RECIP_EMAIL_CC_W](pidtagsearchrecipientemailcc-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-211">**[PR_SEARCH_RECIP_EMAIL_CC_W](pidtagsearchrecipientemailcc-canonical-property.md)**</span></span>
    
- <span data-ttu-id="460fe-212">**[PR_SEARCH_RECIP_EMAIL_TO_W](pidtagsearchrecipientemailto-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="460fe-212">**[PR_SEARCH_RECIP_EMAIL_TO_W](pidtagsearchrecipientemailto-canonical-property.md)**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="460fe-213">関連項目</span><span class="sxs-lookup"><span data-stu-id="460fe-213">See also</span></span>

- [<span data-ttu-id="460fe-214">Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアにアクセスする</span><span class="sxs-lookup"><span data-stu-id="460fe-214">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)  
- [<span data-ttu-id="460fe-215">Outlook プロファイルで Exchange Server のバージョンを検出する</span><span class="sxs-lookup"><span data-stu-id="460fe-215">Detect the Version of Exchange Server in an Outlook Profile</span></span>](how-to-detect-the-version-of-exchange-server-in-an-outlook-profile.md)
- [<span data-ttu-id="460fe-216">Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアを開く</span><span class="sxs-lookup"><span data-stu-id="460fe-216">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="460fe-217">Exchange キャッシュ モードで同期を呼び出すことなく OST でメッセージを管理する</span><span class="sxs-lookup"><span data-stu-id="460fe-217">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

