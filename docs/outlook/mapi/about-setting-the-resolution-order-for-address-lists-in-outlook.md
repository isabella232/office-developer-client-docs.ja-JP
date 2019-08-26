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
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a>Outlook でのアドレス一覧の解決順序の設定について

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Microsoft Office Outlook では、各プロファイルについて複数のアドレス一覧をサポートしており、ユーザーはメール メッセージの受信者や出席依頼を受けた会議出席者を解決する、アドレス一覧の順序を手動で指定できます。 たとえば、まず Outlook アドレス帳に対して、その次にグローバル アドレス一覧に対して名前の解決を行うというような解決順序を設定することができます。 コンピューターでは、ユーザーがアドレス帳を開き、**ツール**、続いて**オプション**をクリックして、解決順序を指定することができます。 ただし、企業環境では、IT 管理者が名前の解決が行われるアドレス一覧の順序をプログラムで設定する方が効率的です。 このようなコードは、管理者が企業内で展開するスタートアップ自動化スクリプトの一部として使用することができます。 
  
MAPI は、**[IAddrBook](iaddrbookimapiprop.md)** インターフェイスの **[SetSearchPath](iaddrbook-getsearchpath.md)** メソッドをサポートするため、名前の解決に使用するプロファイルに新しい検索パスを設定することができます。**IAddrBook::SetSearchPath** メソッドを使用するには、関連するアドレス帳のコンテナーを解決すべき順序で保持する配列を使用し、目的の解決順序を指定する必要があります。配列内の各エントリには、対応するアドレス帳のエントリ ID も含める必要があります。 
  
アドレス一覧のカスタム検索パスを指定するためのコード例を次に示します。
  
- [アドレス一覧の解決順序をプログラムにより設定する](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [KB 292590: SetSearchPath を使用してアドレス帳の並べ替え順序を変更する方法](https://support.microsoft.com/kb/292590)
    

