---
title: Outlook でのアドレス一覧の解決順序の設定について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
description: '最終更新日: 2012 年 7 月 5 日'
ms.openlocfilehash: 07a4c3e90f686f291f95ff87f337b54d8bf35edc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391410"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a><span data-ttu-id="53eb7-103">Outlook でのアドレス一覧の解決順序の設定について</span><span class="sxs-lookup"><span data-stu-id="53eb7-103">About Setting the Resolution Order for Address Lists in Outlook</span></span>

  
  
<span data-ttu-id="53eb7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53eb7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53eb7-105">Microsoft Office Outlook では、各プロファイルについて複数のアドレス一覧をサポートしており、ユーザーは電子メール メッセージの受信者や出席依頼を受けた会議出席者を解決する、アドレス一覧の順序を手動で指定できます。</span><span class="sxs-lookup"><span data-stu-id="53eb7-105">For each profile, Microsoft Office Outlook supports multiple address lists and users can manually specify the order of address lists by which recipients in email messages and attendees in meeting requests are resolved.</span></span> <span data-ttu-id="53eb7-106">たとえば、まず Outlook アドレス帳に対して、その次にグローバル アドレス一覧に対して名前の解決を行うというような解決順序を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="53eb7-106">For example, you can set the resolution order so that names are resolved first against your Outlook Address Book, and then against the Global Address List.</span></span> <span data-ttu-id="53eb7-107">コンピューターでは、ユーザーがアドレス帳を開き、**ツール**、続いて**オプション**をクリックして、解決順序を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="53eb7-107">On a computer, a user can open the Address Book, click **Tools** and then **Options** to specify this resolution order.</span></span> <span data-ttu-id="53eb7-108">ただし、企業環境では、IT 管理者が名前の解決が行われるアドレス一覧の順序をプログラムで設定する方が効率的です。</span><span class="sxs-lookup"><span data-stu-id="53eb7-108">However, in a corporate environment, it is more efficient for IT administrators to programmatically set the order of address lists by which names are resolved.</span></span> <span data-ttu-id="53eb7-109">このようなコードは、管理者が企業内で展開するスタートアップ自動化スクリプトの一部として使用することができます。</span><span class="sxs-lookup"><span data-stu-id="53eb7-109">Such code can be used as part of a startup automation script that an administrator deploys inside the corporation.</span></span> 
  
<span data-ttu-id="53eb7-110">MAPI は、**[IAddrBook](iaddrbookimapiprop.md)** インターフェイスの**[SetSearchPath](iaddrbook-getsearchpath.md)** メソッドをサポートするため、名前の解決に使用するプロファイルに新しい検索パスを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="53eb7-110">MAPI supports the **[SetSearchPath](iaddrbook-getsearchpath.md)** method in the **[IAddrBook](iaddrbookimapiprop.md)** interface, which allows you to set a new search path in the profile that is used for name resolution.</span></span> <span data-ttu-id="53eb7-111">**IAddrBook::SetSearchPath**メソッドを使用するには、解決されるべき順序に並んだ該当のアドレス帳のコンテナーを格納する配列を使って、希望する解決順序を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53eb7-111">To use the **IAddrBook::SetSearchPath** method, you must specify the desired resolution order by using an array that holds containers of the relevant address books in the order they should be resolved.</span></span> <span data-ttu-id="53eb7-112">配列内の各エントリには、対応するアドレス帳のエントリ ID も含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="53eb7-112">Each entry in that array should also contain the entry ID of the corresponding address book.</span></span> 
  
<span data-ttu-id="53eb7-113">アドレス一覧のカスタム検索パスを指定するためのコード例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="53eb7-113">The following are code examples of how to specify a custom search path for address lists.</span></span>
  
- [<span data-ttu-id="53eb7-114">アドレス一覧の解決順序をプログラムにより設定する</span><span class="sxs-lookup"><span data-stu-id="53eb7-114">Programmatically set the resolution order for address lists</span></span>](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [<span data-ttu-id="53eb7-115">KB 292590: SetSearchPathを使用してアドレス帳の並べ替え順序を変更する方法</span><span class="sxs-lookup"><span data-stu-id="53eb7-115">KB 292590: How To Change Address Book Sort Order with SetSearchPath</span></span>](https://support.microsoft.com/kb/292590)
    

