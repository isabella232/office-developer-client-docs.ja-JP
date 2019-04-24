---
title: ������ Exchange �A�J�E���g��g�p���܂��B
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4e1804bf-4c50-4942-a7ab-9a8caf1be7e5
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: a5792ebaf78d77924bc3157be63d937b66e9f4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329654"
---
# <a name="using-multiple-exchange-accounts"></a><span data-ttu-id="51517-103">������ Exchange �A�J�E���g��g�p���܂��B</span><span class="sxs-lookup"><span data-stu-id="51517-103">Using Multiple Exchange Accounts</span></span>

  
  
<span data-ttu-id="51517-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51517-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51517-105">microsoft outlook 2010 および microsoft outlook 2013 は、複数の exchange 電子メールアカウントとの統合をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="51517-105">Microsoft Outlook 2010 and Microsoft Outlook 2013 support integration with multiple exchange email accounts.</span></span> <span data-ttu-id="51517-106">outlook 2010 または outlook 2013 では、ユーザーは2つの exchange アカウントを同じプロファイルに追加しても、公開されたグローバルアドレス一覧 (GAL)、exchange の不在構成、フォルダー共有などの豊富な exchange 機能を利用できます。</span><span class="sxs-lookup"><span data-stu-id="51517-106">In Outlook 2010 or Outlook 2013, a user could add two exchange accounts to the same profile and still enjoy rich Exchange features such as the published global address list (GAL), Exchange Out-of-Office configuration, and folder sharing.</span></span>
  
<span data-ttu-id="51517-107">Microsoft Office Outlook 2007 以前の MAPI プロファイルセクションに精通しているユーザーは、電子メールユーザー名やサーバー名などの exchange 設定が、固定 exchange グローバルプロファイルセクション**pbGlobalProfileSectionGuid**に保存されていることがわかっています。</span><span class="sxs-lookup"><span data-stu-id="51517-107">Those familiar with the MAPI profile sections for Microsoft Office Outlook 2007 and earlier know that Exchange settings, such as the email user name and server name, are stored in the fixed Exchange Global Profile section, **pbGlobalProfileSectionGuid**.</span></span> <span data-ttu-id="51517-108">outlook 2010 および outlook 2013 では、設定を保存するためにそれぞれの Exchange アカウントに独自のプロファイルセクションが必要で、 **pbGlobalProfileSectionGuid**が使用できなくなりました。</span><span class="sxs-lookup"><span data-stu-id="51517-108">In Outlook 2010 and Outlook 2013, each Exchange account needs its own profile section to store settings, making the **pbGlobalProfileSectionGuid** obsolete.</span></span> 
  
<span data-ttu-id="51517-p103">�v���t�@�C��] �ŁA Outlook 2010��Outlook 2013 Exchange �̐ݒ肪�܂��ۑ�����Ă��邪�A�v���t�@�C�����Ƃ̐ݒ��܂ރZ�N�V�����̃v���t�@�C���̈�ӂ̎��ʎq�����蓖�Ă��Ă��铮�I�ɕύX���܂��B�v���t�@�C���� Exchange �̐ݒ�̏ꏊ�́A[ [PidTagExchangeProfileSectionId ���K���̃v���p�e�B](pidtagexchangeprofilesectionid-canonical-property.md)] �́AExchange �A�J�E���g�̃��b�Z�[�W �T�[�r�X �v���t�@�C��] �Z�N�V�����ɋL�ڂ���Ă���ɕۑ�����܂��B���̃v���p�e�B�́A������Ƃ̏ꍇ�́A���̃��b�Z�[�W �T�[�r�X�̃v���o�C�_�[���Ƃ� [�v���t�@�C��] �Z�N�V�����ɂ�L�ڂ���Ă��܂��B��ӂ̎��ʎq�́A�T�[�o�[�ɕۑ�����Ă��Ȃ��ƁA�v���t�@�C���ňقȂ邪���܂��B</span><span class="sxs-lookup"><span data-stu-id="51517-p103">Outlook 2010 and Outlook 2013 Exchange settings are still stored in the profile, but a unique identifier for the profile section that contains their settings is dynamically allocated per profile. The location of the Exchange settings in the profile is stored in the [PidTagExchangeProfileSectionId Canonical Property](pidtagexchangeprofilesectionid-canonical-property.md), which can be found in the message service profile section of the Exchange account. This property can also be found in the profile section for each provider in this message service of the account. The unique identifier is not stored on the server and will be different across profiles.</span></span>
  
<span data-ttu-id="51517-p104">Outlook 2010Outlook 2013 **PidTagExchangeProfileSectionId**��ӂ̎��ʎq�Ƃ��Ă�g���� Exchange �A�J�E���g��w�肵�܂��B���̕��@�Ŏg�p����ꍇ�A��ӂ̎��ʎq�� **emsmdbUID**�ƌĂ΂�܂��BMAPI �����Outlook����ɂ���āA **emsmdbUID**������Ɏg�p���� Exchange �A�J�E���g��w�肷��K�v����܂��B</span><span class="sxs-lookup"><span data-stu-id="51517-p104">Outlook 2010 and Outlook 2013 use the **PidTagExchangeProfileSectionId** as a unique identifier to specify an Exchange account. When used in this manner, this unique identifier is known as the **emsmdbUID**. For some MAPI and Outlook operations, an **emsmdbUID** might be required to specify which Exchange account should be used for the operation.</span></span> 
  
<span data-ttu-id="51517-p105">������ Exchange �A�J�E���g��T�|�[�g���邽�߂ɁA�R�[�h�̈ꕔ�̐V�����֐��̌Ăяo����g�p���Ă��������B**IMailUser: IMAPIProp**�ƁA���̊֐��� 1 ��[IDistList: IMAPIContainer](iaddrbook-openentry.md)�� [entryID](iaddrbook-compareentryids.md)��[IAddrBook::OpenEntry](imailuserimapiprop.md)�܂���[IAddrBook::CompareEntryIDs](idistlistimapicontainer.md)��g�p���Ă��邷�ׂĂ̌Ăяo����u�������܂��B</span><span class="sxs-lookup"><span data-stu-id="51517-p105">In order to support multiple Exchange accounts, you must use some calls to new functions in your code. Replace any call that uses an **entryID** and either [IAddrBook::OpenEntry](iaddrbook-openentry.md) or [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) on [IMailUser : IMAPIProp](imailuserimapiprop.md) and [IDistList : IMAPIContainer](idistlistimapicontainer.md) with one of the following functions.</span></span> 
  
- [<span data-ttu-id="51517-118">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="51517-118">HrCompareABEntryIDsWithExchangeContext</span></span>](hrcompareabentryidswithexchangecontext.md)
    
- [<span data-ttu-id="51517-119">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="51517-119">HrDoABDetailsWithExchangeContext</span></span>](hrdoabdetailswithexchangecontext.md)
    
- [<span data-ttu-id="51517-120">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="51517-120">HrDoABDetailsWithProviderUID</span></span>](hrdoabdetailswithprovideruid.md)
    
- [<span data-ttu-id="51517-121">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="51517-121">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)
    
- [<span data-ttu-id="51517-122">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="51517-122">HrOpenABEntryUsingDefaultContext</span></span>](hropenabentryusingdefaultcontext.md)
    
- [<span data-ttu-id="51517-123">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="51517-123">HrOpenABEntryWithExchangeContext</span></span>](hropenabentrywithexchangecontext.md)
    
- [<span data-ttu-id="51517-124">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="51517-124">HrOpenABEntryWithProviderUID</span></span>](hropenabentrywithprovideruid.md)
    
- [<span data-ttu-id="51517-125">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="51517-125">HrOpenABEntryWithProviderUIDSupport</span></span>](hropenabentrywithprovideruidsupport.md)
    
- [<span data-ttu-id="51517-126">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="51517-126">HrOpenABEntryWithResolvedRow</span></span>](hropenabentrywithresolvedrow.md)
    
- [<span data-ttu-id="51517-127">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="51517-127">HrOpenABEntryWithSupport</span></span>](hropenabentrywithsupport.md)
    
## <a name="legacy-support"></a><span data-ttu-id="51517-128">�]���̃T�|�[�g</span><span class="sxs-lookup"><span data-stu-id="51517-128">Legacy support</span></span>

<span data-ttu-id="51517-p106">���̐V���� **emsmdbUID**�Z�N�V������쐬����O�ɋL�q MAPI �N���C�A���g�͈��������T�|�[�g����܂��B�����̃N���C�A���g�͈��������O���[�o���O�̃Z�N�V���� **pbGlobalProfileSectionGuid**��擾���܂��B���̃v���t�@�C��] �Z�N�V�����̃N�G���́A�]���̏Ɖ��������� 1 �̎w�肳�ꂽ Exchange �A�J�E���g�Ƀ��_�C���N�g����܂��B�]���̌Ăяo�����������A�J�E���g�́A���b�Z�[�W �T�[�r�X �e�[�u������āAPR_EMSMDB_LEGACY �̗��ǉ����Ċm�F�ł��܂��B1 �̃��b�Z�[�W �T�[�r�X�݂͂̂ɐݒ肳��A���� **PidTagExchangeProfileSectionId** true �̏ꍇ�A����́A�]���� **emsmdbUID**�ƌĂ΂�܂��B</span><span class="sxs-lookup"><span data-stu-id="51517-p106">Any MAPI clients written before the creation of this new **emsmdbUID** section are still supported. These clients will continue to retrieve the previous global section, **pbGlobalProfileSectionGuid**. Queries for this profile section will be redirected to one designated Exchange account that handles legacy inquiries. The account that handles the legacy calls can be determined by looking at the message service table and adding a column for PR_EMSMDB_LEGACY. Only one message service will have this set to true, and its **PidTagExchangeProfileSectionId** is called the legacy **emsmdbUID**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="51517-p107">[!����] ����̃X�g�A�Ɗ���̃A�J�E���g�Ȃǂ� MAPI �ݒ�́A�A�J�E���g���]���̌Ăяo����������邽�߂̉e����^����Ȃ��B�]���̌Ăяo�����������A�J�E���g��\�����邱�Ƃ͂ł��܂���B</span><span class="sxs-lookup"><span data-stu-id="51517-p107">Configurable MAPI settings such as the default store and the default account have no effect on which account handles legacy calls. The account that handles the legacy calls cannot be configured.</span></span> 
  
<span data-ttu-id="51517-p108">�]���̃A�J�E���g�� **emsmdbUID**��Outlook�O���[�o�� �v���t�@�C��] �Z�N�V�����ɃR�s�[����܂��B���̃v���p�e�B�����݂��Ȃ��ꍇ�A���b�Z�[�W�̃T�[�r�X�̃e�[�u���̃N�G������s����ƁA�ǂ̂悤�ȃA�J�E���g���A�]���̃n���h���[�ł��邱�Ƃ�m�F���A Outlook�O���[�o�� �v���t�@�C��] �Z�N�V�����Œl��ݒ肵�܂��B</span><span class="sxs-lookup"><span data-stu-id="51517-p108">The **emsmdbUID** of the legacy account is copied to the Outlook Global Profile Section. If this property does not exist, querying for the message services table will determine what account is the legacy handler and set the value in the Outlook Global Profile Section.</span></span> 
  
<span data-ttu-id="51517-p109">�I�t�ɂ���ƁAExchange �O���[�o�� �v���t�@�C�� �Z�N�V��������O���[�o�� �v���t�@�C��] �Z�N�V�������قȂ�Outlook����Outlook 2010�����Outlook 2013�� Exchange �̃O���[�o�� �v���t�@�C��] �Z�N�V�����͂���܂���O���[�o���{���ɕ����� Exchange �A�J�E���g�����邱�Ƃ��ł��܂��BOutlook�O���[�o�� �v���t�@�C��] �Z�N�V�����ɂ́A Outlook�A�ŋߎg�p�����t�H���_�[�̏�ԁA�܂��̓O���[�o���ڑ��̏�ԂȂǂ̃v���p�e�B���܂܂�Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="51517-p109">To be clear, the Outlook Global Profile Section differs from the Exchange Global Profile Section, and in Outlook 2010 and Outlook 2013 the Exchange Global Profile Section is no longer really global because you can have multiple Exchange accounts. The Outlook Global Profile section contains properties about Outlook, such as the state of the folder MRU or the state of the global connection.</span></span>
  
## <a name="address-book-account-contexts"></a><span data-ttu-id="51517-140">�A�h���X���̃A�J�E���g�̃R���e�L�X�g</span><span class="sxs-lookup"><span data-stu-id="51517-140">Address Book Account Contexts</span></span>

<span data-ttu-id="51517-141">������ Exchange �A�J�E���g�Ő������A�h���X��������ɂ́A�A�h���X���ɒʘb�������� Exchange �A�J�E���g������ł���悤�ɁA�A�J�E���g�̃R���e�L�X�g���V�����@�\��g�p���܂��B</span><span class="sxs-lookup"><span data-stu-id="51517-141">To resolve addresses correctly with multiple Exchange accounts, use the new functions that take an account context so that calls to the address book search the correct Exchange account.</span></span>
  
<span data-ttu-id="51517-p110">Api ���ꂽ�@�\������S�ɕ����� Exchange �ł͂Ȃ����߂ɁA�������O�̃A�h���X���� Api �͔p�~����܂����B���̃A�J�E���g�̃R���e�L�X�g�́A�ʏ�A **emsmdbUID**�ł��B</span><span class="sxs-lookup"><span data-stu-id="51517-p110">Some previous address book APIs were deprecated because the APIs were not fully multiple Exchange capable. This account context is usually an **emsmdbUID**.</span></span>
  
<span data-ttu-id="51517-144">������ Exchange �A�J�E���g�ɂ́A **emsmdbUID**�ł́A�ɉ����āA **emsabpUID**�������܂��B</span><span class="sxs-lookup"><span data-stu-id="51517-144">In addition to the **emsmdbUID**, multiple Exchange accounts also have an **emsabpUID**.</span></span>
  
1. <span data-ttu-id="51517-145">**emsmdbUID**�l�́A�A�J�E���g�̃R���e�L�X�g������܂��B</span><span class="sxs-lookup"><span data-stu-id="51517-145">The **emsmdbUID** value identifies the account context.</span></span> 
    
2. <span data-ttu-id="51517-146">**emsabpUID**�l�́AExchange �A�h���X��������܂��B</span><span class="sxs-lookup"><span data-stu-id="51517-146">The **emsabpUID** value identifies an Exchange address book provider.</span></span> 
    
<span data-ttu-id="51517-p111">**emsabpUID**�l�͒ʏ�A��M�҂�������Ƃ��Ɏg�p����܂��B[IAddrBook::ResolveName](iaddrbook-resolvename.md)��g�p���Ď�M�҂�������ɂ́AExchange ��M�҂̍s�ɂ́A **emsabpUID**�l��܂ށA **PR_AB_PROVIDERS** (0x3D010102) �v���p�e�B���܂܂�Ă��܂��B���� **emsabpUID**�l�́A����̎�M�҂� Exchange �A�h���X����w�肵�܂��B</span><span class="sxs-lookup"><span data-stu-id="51517-p111">The **emsabpUID** value is typically used when resolving a recipient. When resolving a recipient using [IAddrBook::ResolveName](iaddrbook-resolvename.md), an Exchange recipient row contains the **PR_AB_PROVIDERS** (0x3D010102) property, which contains the **emsabpUID** value. This **emsabpUID** value identifies the Exchange address book provider for the specific recipient.</span></span> 
  
<span data-ttu-id="51517-150">����� **emsmdbUID** **emsabpUID**�l��w�肷��ꍇ�́A **emsmdbUID**�̃v���t�@�C���̃Z�N�V������J���A **PR_EMSABP_USER_UID** (0x0x3D1A0102) �̃v���p�e�B��擾���܂��B</span><span class="sxs-lookup"><span data-stu-id="51517-150">If you want to determine the **emsabpUID** value for a particular **emsmdbUID**, open up the profile section for the **emsmdbUID** and get the **PR_EMSABP_USER_UID** (0x0x3D1A0102) property.</span></span> 
  
<span data-ttu-id="51517-p112">[IAddrBook::PrepareRecips](iaddrbook-preparerecips.md)�A�Ăяo���ꍇ�������X�g��� Exchange ��M�҂��A��M�҂���������A�h���X���ɑΉ����� **emsabpUID**�� **PR_AB_PROVIDERS**�v���p�e�B���܂܂�Ă��邱�Ƃ�m�F���܂��B�ǉ��̑����K�v�Ƃ��Ȃ�[IAddrBook::ResolveName](iaddrbook-preparerecips.md)����擾�����s��[IAddrBook::PrepareRecips](iaddrbook-resolvename.md)��Ăяo�����Ƃ��������̃R�[�h�ɓd�b�������[IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) **PR_ENTRYID**�v���p�e�B�݂̂��܂܂�Ă���s�B���̍s�Ɠ����悤�ȏ󋵂� **PR_AB_PROVIDERS**�v���p�e�B�ɓK�؂� **emsabpUID**�� **PR_ENTRYID**�� **PR_AB_PROVIDERS**�̗�����܂߂�K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="51517-p112">If you are calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), make sure that the Exchange recipients in the list that you pass in contain the **PR_AB_PROVIDERS** property that has the **emsabpUID** that corresponds to the address book provider that the recipient belongs to. Calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on a row that you obtained from [IAddrBook::ResolveName](iaddrbook-resolvename.md) requires no additional action, but some code will call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on rows that contain only the **PR_ENTRYID** property. Rows in this and similar situations should contain both **PR_ENTRYID** and **PR_AB_PROVIDERS** with the **PR_AB_PROVIDERS** property set to the correct **emsabpUID**.</span></span>
  
<span data-ttu-id="51517-154">������ Exchange �A�J�E���g�������邽�߂̃v���Z�X�̊ȒP�Ȑ���́A���̂Ƃ���ł��B</span><span class="sxs-lookup"><span data-stu-id="51517-154">A simple description of the process for resolving multiple Exchange accounts is as follows:</span></span>
  
- <span data-ttu-id="51517-p113">�T�[�r�X�̈�ӂ̎��ʎq��w�肷��ɂ́A�R�[�h�́A **PR_SERVICE_UID**�v���p�e�B�������̂ƈ�v���郁�b�Z�[�W �X�g�A�̃e�[�u���Ō������܂��B��������́A������ **PR_MDB_PROVIDER**��w��ł��܂��B���̍s�ɂ́A�K�؂ȃX�g�A���܂܂�Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="51517-p113">Given the service unique identifier, your code looks in the table of the message store of the **PR_SERVICE_UID** property that matches the one that you have. From there, you can determine the correct **PR_MDB_PROVIDER**. This row contains the appropriate store.</span></span>
    
- <span data-ttu-id="51517-158">�R�[�h�� **emsmdbUID**��w�肷��ƁA **emsmdbUID**�Ɉ�v���� **PidTagExchangeProfileSectionId**����J����s�̃��b�Z�[�W �T�[�r�X �e�[�u�����\������܂��B</span><span class="sxs-lookup"><span data-stu-id="51517-158">Given an **emsmdbUID**, your code looks in the message services table for the row that exposes the **PidTagExchangeProfileSectionId** that matches the **emsmdbUID**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="51517-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="51517-159">See also</span></span>



[<span data-ttu-id="51517-160">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="51517-160">HrCompareABEntryIDsWithExchangeContext</span></span>](hrcompareabentryidswithexchangecontext.md)
  
[<span data-ttu-id="51517-161">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="51517-161">HrDoABDetailsWithExchangeContext</span></span>](hrdoabdetailswithexchangecontext.md)
  
[<span data-ttu-id="51517-162">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="51517-162">HrDoABDetailsWithProviderUID</span></span>](hrdoabdetailswithprovideruid.md)
  
[<span data-ttu-id="51517-163">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="51517-163">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)
  
[<span data-ttu-id="51517-164">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="51517-164">HrOpenABEntryUsingDefaultContext</span></span>](hropenabentryusingdefaultcontext.md)
  
[<span data-ttu-id="51517-165">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="51517-165">HrOpenABEntryWithExchangeContext</span></span>](hropenabentrywithexchangecontext.md)
  
[<span data-ttu-id="51517-166">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="51517-166">HrOpenABEntryWithProviderUID</span></span>](hropenabentrywithprovideruid.md)
  
[<span data-ttu-id="51517-167">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="51517-167">HrOpenABEntryWithProviderUIDSupport</span></span>](hropenabentrywithprovideruidsupport.md)
  
[<span data-ttu-id="51517-168">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="51517-168">HrOpenABEntryWithResolvedRow</span></span>](hropenabentrywithresolvedrow.md)
  
[<span data-ttu-id="51517-169">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="51517-169">HrOpenABEntryWithSupport</span></span>](hropenabentrywithsupport.md)
  
[<span data-ttu-id="51517-170">PidTagExchangeProfileSectionId ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="51517-170">PidTagExchangeProfileSectionId Canonical Property</span></span>](pidtagexchangeprofilesectionid-canonical-property.md)


<span data-ttu-id="51517-171">[[�O���[�o�� �v���t�@�C��] �Z�N�V������J�����@](https://support.microsoft.com/kb/188482)</span><span class="sxs-lookup"><span data-stu-id="51517-171">[How To Open the Global Profile Section](https://support.microsoft.com/kb/188482)</span></span>

