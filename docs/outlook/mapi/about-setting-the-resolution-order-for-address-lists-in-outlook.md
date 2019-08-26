---
title: Outlook でのアドレス一覧の解決順序の設定について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
description: '最終更新日: 2012 年 7 月 5 日'
ms.openlocfilehash: 07a4c3e90f686f291f95ff87f337b54d8bf35edc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321834"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a><span data-ttu-id="3915b-103">Outlook でのアドレス一覧の解決順序の設定について</span><span class="sxs-lookup"><span data-stu-id="3915b-103">About Setting the Resolution Order for Address Lists in Outlook</span></span>

  
  
<span data-ttu-id="3915b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3915b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3915b-105">Microsoft Office Outlook では、各プロファイルについて複数のアドレス一覧をサポートしており、ユーザーはメール メッセージの受信者や出席依頼を受けた会議出席者を解決する、アドレス一覧の順序を手動で指定できます。</span><span class="sxs-lookup"><span data-stu-id="3915b-105">For each profile, Microsoft Office Outlook supports multiple address lists and users can manually specify the order of address lists by which recipients in email messages and attendees in meeting requests are resolved.</span></span> <span data-ttu-id="3915b-106">たとえば、まず Outlook アドレス帳に対して、その次にグローバル アドレス一覧に対して名前の解決を行うというような解決順序を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="3915b-106">For example, you can set the resolution order so that names are resolved first against your Outlook Address Book, and then against the Global Address List.</span></span> <span data-ttu-id="3915b-107">コンピューターでは、ユーザーがアドレス帳を開き、**ツール**、続いて**オプション**をクリックして、解決順序を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="3915b-107">On a computer, a user can open the Address Book, click **Tools** and then **Options** to specify this resolution order.</span></span> <span data-ttu-id="3915b-108">ただし、企業環境では、IT 管理者が名前の解決が行われるアドレス一覧の順序をプログラムで設定する方が効率的です。</span><span class="sxs-lookup"><span data-stu-id="3915b-108">However, in a corporate environment, it is more efficient for IT administrators to programmatically set the order of address lists by which names are resolved.</span></span> <span data-ttu-id="3915b-109">このようなコードは、管理者が企業内で展開するスタートアップ自動化スクリプトの一部として使用することができます。</span><span class="sxs-lookup"><span data-stu-id="3915b-109">Such code can be used as part of a startup automation script that an administrator deploys inside the corporation.</span></span> 
  
<span data-ttu-id="3915b-p102">MAPI は、**[IAddrBook](iaddrbookimapiprop.md)** インターフェイスの **[SetSearchPath](iaddrbook-getsearchpath.md)** メソッドをサポートするため、名前の解決に使用するプロファイルに新しい検索パスを設定することができます。**IAddrBook::SetSearchPath** メソッドを使用するには、関連するアドレス帳のコンテナーを解決すべき順序で保持する配列を使用し、目的の解決順序を指定する必要があります。配列内の各エントリには、対応するアドレス帳のエントリ ID も含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="3915b-p102">MAPI supports the **[SetSearchPath](iaddrbook-getsearchpath.md)** method in the **[IAddrBook](iaddrbookimapiprop.md)** interface, which allows you to set a new search path in the profile that is used for name resolution. To use the **IAddrBook::SetSearchPath** method, you must specify the desired resolution order by using an array that holds containers of the relevant address books in the order they should be resolved. Each entry in that array should also contain the entry ID of the corresponding address book.</span></span> 
  
<span data-ttu-id="3915b-113">アドレス一覧のカスタム検索パスを指定するためのコード例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="3915b-113">The following are code examples of how to specify a custom search path for address lists.</span></span>
  
- [<span data-ttu-id="3915b-114">アドレス一覧の解決順序をプログラムにより設定する</span><span class="sxs-lookup"><span data-stu-id="3915b-114">Programmatically Set the Resolution Order for Address Lists</span></span>](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [<span data-ttu-id="3915b-115">KB 292590: SetSearchPath を使用してアドレス帳の並べ替え順序を変更する方法</span><span class="sxs-lookup"><span data-stu-id="3915b-115">KB 292590: How To Change Address Book Sort Order with SetSearchPath</span></span>](https://support.microsoft.com/kb/292590)
    

