---
title: 受信者のプロパティを取得します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 358f892b-54a7-4213-b3c0-94f28f99716f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a48c6a8e043062bc6b48e09934fded1dccb507b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585438"
---
# <a name="retrieving-recipient-properties"></a>受信者のプロパティを取得します。
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a>アドレス帳エントリの 1 つまたは複数のプロパティにアクセスするのには
  
1. 目的のアドレス帳エントリごとに、[アドレス帳コンテナー](iaddrbook-openentry.md)ターゲットのユーザーまたは配布リストをメッセージのエントリ id を渡すことを呼び出します。
    
2. 次のいずれかの操作を行います。
    
   - 取得する 1 つまたは複数のプロパティの一覧で、目的の各アドレス帳エントリには、メッセージングのユーザーまたは配布リストの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出します。 
    
   - [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md)、すべての目的のアドレス帳のエントリのすべてのプロパティを保持する[ADRLIST](adrlist.md)構造体を渡すことを呼び出します。 **PrepareRecips** 1 回の呼び出しは、について、複数のアドレス帳のエントリを返すことができます、ためには、複数の受信者に興味があるとき、という方針です。 
    

