---
title: "Outlook �̃A�h���X�ꗗ�̉\U00011713x�̏�����ݒ肷����@"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
description: '最終更新日: 2012 年 7 月 5 日'
ms.openlocfilehash: d5c4a771417e8556e499e50f3476b08d50157e79
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556995"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a>Outlook でのアドレス一覧の解決順序の設定について

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Microsoft Office Outlook では、各プロファイルについて複数のアドレス一覧をサポートしており、ユーザーはメール メッセージの受信者や出席依頼を受けた会議出席者を解決する、アドレス一覧の順序を手動で指定できます。 たとえば、まず Outlook アドレス帳に対して、その次にグローバル アドレス一覧に対して名前の解決を行うというような解決順序を設定することができます。 コンピューターでは、ユーザーがアドレス帳を開き、**ツール**、続いて **オプション** をクリックして、解決順序を指定することができます。 ただし、企業環境では、IT 管理者が名前の解決が行われるアドレス一覧の順序をプログラムで設定する方が効率的です。 このようなコードは、管理者が企業内で展開するスタートアップ自動化スクリプトの一部として使用することができます。 
  
MAPI supports the **[SetSearchPath](iaddrbook-getsearchpath.md)** method in the **[IAddrBook](iaddrbookimapiprop.md)** interface, which allows you to set a new search path in the profile that is used for name resolution. To use the **IAddrBook::SetSearchPath** method, you must specify the desired resolution order by using an array that holds containers of the relevant address books in the order they should be resolved. Each entry in that array should also contain the entry ID of the corresponding address book. 
  
アドレス一覧のカスタム検索パスを指定するためのコード例を次に示します。
  
- [アドレス一覧の解決順序をプログラムにより設定する](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [KB 292590: SetSearchPath を使用してアドレス帳の並べ替え順序を変更する方法](https://support.microsoft.com/kb/292590)
    

