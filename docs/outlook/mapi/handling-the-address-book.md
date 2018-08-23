---
title: アドレス帳の処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b685244a-fe1b-4416-85d3-4bd86ccbc3aa
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7a72d0e90e6c28874f341fc9ba7af843a44c5da8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583324"
---
# <a name="handling-the-address-book"></a><span data-ttu-id="5dec5-103">アドレス帳の処理</span><span class="sxs-lookup"><span data-stu-id="5dec5-103">Handling the address book</span></span>
  
<span data-ttu-id="5dec5-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5dec5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5dec5-105">MAPI �A�h���X�����������ɂ́A�Z������Q�Ƃ��āA�ύX�����] �Ƀ��b�Z�[�W�̎�M�҂��M�҂̃v���p�e�B��ύX����ꎞ�A�h���X] ��쐬���āA1 �ȏ�̋��ʂ̃A�h���X] �_�C�A���O �{�b�N�X���\�����ꂽ���b�Z�[�W�̃��[�U�[�܂��͔z�z���X�g��ǉ�����Ƃ��Ďg�p����G���g���𒊏o����܂߂邱�Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="5dec5-105">Handling the MAPI address book can include extracting entries to be used as message recipients, modifying recipient properties, adding messaging users or distribution lists, creating one-offs, and displaying one or more of the common address dialog boxes to allow users to browse address information and make changes.</span></span>

- <span data-ttu-id="5dec5-106">[アドレス帳を開く](opening-the-address-book.md): MAPI を使用してアドレス帳を開く方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5dec5-106">[Opening the Address Book](opening-the-address-book.md): Describes how to use MAPI to open an address book.</span></span>
    
- <span data-ttu-id="5dec5-107">[共通のアドレス] ダイアログ ボックスを表示する](displaying-the-common-address-dialog-box.md): 別のアドレス帳コンテナーを表示する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5dec5-107">[Displaying the Common Address Dialog Box](displaying-the-common-address-dialog-box.md): Describes how to display different address book containers.</span></span>
    
- <span data-ttu-id="5dec5-108">[アドレス帳コンテナーを開く](opening-an-address-book-container.md): 別のアドレス帳コンテナーを開く方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5dec5-108">[Opening an Address Book Container](opening-an-address-book-container.md): Describes how to open different address book containers.</span></span>
    
- <span data-ttu-id="5dec5-109">[アドレス帳オプションの設定](setting-address-book-options.md): アドレス帳を使用するためのオプションについて説明するプロパティを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5dec5-109">[Setting Address Book Options](setting-address-book-options.md): Describes how to set the properties that describe options for using the address book.</span></span>
    
- <span data-ttu-id="5dec5-110">[受信者を作成する](creating-a-recipient.md): メッセージをアドレス指定する場合は、受信者を作成する方法について説明し、変更可能なアドレス帳コンテナーにエントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="5dec5-110">[Creating a Recipient](creating-a-recipient.md): Describes how to create recipients when addressing messages and adding entries to modifiable address book containers.</span></span>
    
- <span data-ttu-id="5dec5-111">[配布リストを作成する](creating-a-distribution-list.md): 変更可能なコンテナーに、配布リストを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5dec5-111">[Creating a Distribution List](creating-a-distribution-list.md): Describes how to create a distribution list into a modifiable container.</span></span>
    
- <span data-ttu-id="5dec5-112">[受信者のコピー](copying-a-recipient.md): 別の 1 つのコンテナー、または同じコンテナーからの受信者にコピーする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5dec5-112">[Copying a Recipient](copying-a-recipient.md): Describes how to copy recipients from one container into another or the same container.</span></span>
    
- <span data-ttu-id="5dec5-113">[受信者を削除する](deleting-a-recipient.md): 変更可能なコンテナーから 1 つまたは複数のアドレス帳のエントリを削除する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5dec5-113">[Deleting a Recipient](deleting-a-recipient.md): Describes how to remove one or more address book entries from a modifiable container.</span></span>
    
- <span data-ttu-id="5dec5-114">[受信者を準備する](preparing-a-recipient.md): 長期のエントリ id を短期的なエントリの識別子を変換して可能性のある追加、変更、またはプロパティの順序を変更して、受信者を準備する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5dec5-114">[Preparing a Recipient](preparing-a-recipient.md): Describes how to prepares recipients by converting their short-term entry identifiers to long-term entry identifiers and possibly adding, changing, or reordering properties.</span></span>
    
- <span data-ttu-id="5dec5-115">[配布リストのメンバーへのアクセス](accessing-the-members-of-a-distribution-list.md): 配布リストのメンバーにアクセスする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5dec5-115">[Accessing the Members of a Distribution List](accessing-the-members-of-a-distribution-list.md): Describes how to access the members of a distribution list.</span></span>
    
- <span data-ttu-id="5dec5-116">[受信者のプロパティを取得しています](retrieving-recipient-properties.md): 受信者のアドレス帳のエントリの 1 つまたは複数のプロパティにアクセスする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5dec5-116">[Retrieving Recipient Properties](retrieving-recipient-properties.md): Describes how to access one or more properties of a recipient address book entry.</span></span>
    
- <span data-ttu-id="5dec5-117">[アドレス帳を検索](searching-the-address-book.md): MAPI 検索機能の 2 つのレベルについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5dec5-117">[Searching the Address Book](searching-the-address-book.md): Describes the two levels of MAPI search functionality.</span></span> 
    
- <span data-ttu-id="5dec5-118">[[の検索] ダイアログ ボックスを使用して](using-an-advanced-search-dialog-box.md): アドレス帳コンテナーで、高度な検索機能を実行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5dec5-118">[Using an Advanced Search Dialog Box](using-an-advanced-search-dialog-box.md): Describes how to run an advanced search functionality in an address book container.</span></span>
    
- <span data-ttu-id="5dec5-119">[受信者名を解決する](resolving-a-recipient-name.md): アドレス帳の名前を解決する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5dec5-119">[Resolving a Recipient Name](resolving-a-recipient-name.md): Describes how to resolve a name in an address book.</span></span>
    
- <span data-ttu-id="5dec5-120">[配布リストの展開](expanding-distribution-lists.md): 配布リストを展開するための MAPI メッセージを表示する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5dec5-120">[Expanding Distribution Lists](expanding-distribution-lists.md): Describes how to prompt MAPI to expand a distribution list.</span></span>
    

