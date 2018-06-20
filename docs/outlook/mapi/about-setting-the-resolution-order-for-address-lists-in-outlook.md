---
title: "Outlook �̃A�h���X�ꗗ�̉\U00011713x�̏�����ݒ肷����@"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
description: '�ŏI�X�V��: 2012�N7��5��'
ms.openlocfilehash: cfc640fd419ad030de6922fa61817881caa70d07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799596"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a><span data-ttu-id="e56a1-103">Outlook �̃A�h���X�ꗗ�̉𑜓x�̏�����ݒ肷����@</span><span class="sxs-lookup"><span data-stu-id="e56a1-103">About Setting the Resolution Order for Address Lists in Outlook</span></span>

  
  
<span data-ttu-id="e56a1-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e56a1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e56a1-105">プロファイルごとに複数のアドレス一覧をサポートしている Microsoft Office Outlook と電子メールの受信者がメッセージおよび会議出席依頼に出席者は解決されたアドレス一覧の順序を手動で指定できます。</span><span class="sxs-lookup"><span data-stu-id="e56a1-105">For each profile, Microsoft Office Outlook supports multiple address lists and users can manually specify the order of address lists by which recipients in email messages and attendees in meeting requests are resolved.</span></span> <span data-ttu-id="e56a1-106">たとえば、名が最初に Outlook アドレス帳、およびに対して、グローバル アドレス一覧に解決されるように、解決の順序を設定できます。</span><span class="sxs-lookup"><span data-stu-id="e56a1-106">For example, you can set the resolution order so that names are resolved first against your Outlook Address Book, and then against the Global Address List.</span></span> <span data-ttu-id="e56a1-107">コンピューターでは、ユーザーがアドレス帳を開き、**ツール**と**オプション**をクリックし、この解決の順序を指定します。</span><span class="sxs-lookup"><span data-stu-id="e56a1-107">On a computer, a user can open the Address Book, click **Tools** and then **Options** to specify this resolution order.</span></span> <span data-ttu-id="e56a1-108">ただし、企業環境でプログラムを使用して、名前が解決されるアドレス一覧の順序を設定するのには IT 管理者の方が効率的です。</span><span class="sxs-lookup"><span data-stu-id="e56a1-108">However, in a corporate environment, it is more efficient for IT administrators to programmatically set the order of address lists by which names are resolved.</span></span> <span data-ttu-id="e56a1-109">このようなコードは、管理者が企業内に展開する起動自動化スクリプトの一部として使用できます。</span><span class="sxs-lookup"><span data-stu-id="e56a1-109">Such code can be used as part of a startup automation script that an administrator deploys inside the corporation.</span></span> 
  
<span data-ttu-id="e56a1-110">MAPI には、 **[IAddrBook](iaddrbookimapiprop.md)** インターフェイスは、名前解決に使用されるプロファイルに新しい検索パスを設定することで、 **[SetSearchPath](iaddrbook-getsearchpath.md)** メソッドがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="e56a1-110">MAPI supports the **[SetSearchPath](iaddrbook-getsearchpath.md)** method in the **[IAddrBook](iaddrbookimapiprop.md)** interface, which allows you to set a new search path in the profile that is used for name resolution.</span></span> <span data-ttu-id="e56a1-111">**IAddrBook::SetSearchPath**メソッドを使用するには、関連のアドレスのコンテナーを保持する配列を使用して、目的の解像度の順序がそれらを解決する順序で書籍を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e56a1-111">To use the **IAddrBook::SetSearchPath** method, you must specify the desired resolution order by using an array that holds containers of the relevant address books in the order they should be resolved.</span></span> <span data-ttu-id="e56a1-112">その配列内の各エントリには、対応するアドレス帳のエントリ ID を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="e56a1-112">Each entry in that array should also contain the entry ID of the corresponding address book.</span></span> 
  
<span data-ttu-id="e56a1-113">�A�h���X�ꗗ�� [�J�X�^�������p�X��w�肷����@�̗����Ɏ����܂��B</span><span class="sxs-lookup"><span data-stu-id="e56a1-113">The following are code examples of how to specify a custom search path for address lists.</span></span>
  
- [<span data-ttu-id="e56a1-114">アドレス一覧の解決の順序をプログラムで設定します。</span><span class="sxs-lookup"><span data-stu-id="e56a1-114">Programmatically Set the Resolution Order for Address Lists</span></span>](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [<span data-ttu-id="e56a1-115">KB 292590: SetSearchPath �ƃA�h���X���̕��בւ�������ύX������@</span><span class="sxs-lookup"><span data-stu-id="e56a1-115">KB 292590: How To Change Address Book Sort Order with SetSearchPath</span></span>](http://support.microsoft.com/kb/292590)
    

