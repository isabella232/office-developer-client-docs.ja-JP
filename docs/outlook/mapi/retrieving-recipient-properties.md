---
title: 受信者のプロパティの取得
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 358f892b-54a7-4213-b3c0-94f28f99716f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 38063cebe70b153decce6713ac5fc31d6916dbf6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426675"
---
# <a name="retrieving-recipient-properties"></a>受信者のプロパティの取得
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a>アドレス帳エントリの1つまたは複数のプロパティにアクセスするには
  
1. 対象のアドレス帳のエントリごとに、 [IAddrBook:: openentry](iaddrbook-openentry.md)を呼び出して、対象のメッセージングユーザーまたは配布リストのエントリ識別子を渡します。
    
2. その後、次のいずれかの操作を行います。
    
   - 対象のアドレス帳エントリごとに、メッセージユーザーまたは配布リストの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、取得する1つまたは複数のプロパティの一覧を指定します。 
    
   - [IAddrBook::P reparerecips](iaddrbook-preparerecips.md)を呼び出し、必要なすべてのアドレス帳エントリのすべてのプロパティを保持する[adrlist](adrlist.md)構造体を渡します。 **PrepareRecips**の1回の呼び出しで複数のアドレス帳エントリの情報が返される可能性があるため、複数の受信者に関心がある場合は、この方法をお勧めします。 
    

