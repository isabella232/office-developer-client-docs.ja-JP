---
title: 受信者のプロパティの取得
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 358f892b-54a7-4213-b3c0-94f28f99716f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ecf340bcf63048ad8d29ba411aa3553e4890bf78
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599117"
---
# <a name="retrieving-recipient-properties"></a>受信者のプロパティの取得
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a>アドレス帳エントリの 1 つ以上のプロパティにアクセスするには
  
1. 対象のアドレス帳エントリごとに [、IAddrBook::OpenEntry](iaddrbook-openentry.md)を呼び出し、ターゲット メッセージング ユーザーまたは配布リストのエントリ識別子を渡します。
    
2. 次に、次のいずれかを実行します。
    
   - メッセージング ユーザーまたは配布リストの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを、取得する 1 つ以上のプロパティの一覧で、関心のあるアドレス帳エントリごとに呼び出します。 
    
   - [IAddrBook::P repareRecips](iaddrbook-preparerecips.md)を呼び出し、必要なすべてのアドレス帳エントリのすべてのプロパティを保持する[ADRLIST](adrlist.md)構造体を渡します。 **PrepareRecips** を呼び出す 1 つの呼び出しは、複数のアドレス帳エントリの情報を返す可能性があるから、複数の受信者に関心がある場合に、この方法が望ましい戦略です。 
    

