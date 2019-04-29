---
title: MAPI レコードおよび検索キー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: caa7b7f3-a5a1-4f07-98c9-22652ecd5d21
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b1b4c0087cecd9164fc96ce7c5b5415f75dbfb03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434565"
---
# <a name="mapi-record-and-search-keys"></a>MAPI レコードおよび検索キー

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
レコードキーと検索キーは、多くの MAPI オブジェクトに割り当てられているバイナリ識別子です。 オブジェクトのエントリ識別子とは異なり、そのレコードまたは検索キーは直接、または、にも対応しています。 
  
## <a name="record-keys"></a>レコードキー

レコードキーは、2つのオブジェクトを比較するために使用されます。 メッセージストアオブジェクトとアドレス帳オブジェクトは、 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) プロパティに格納されているレコードキーを持っている必要があります。 record キーはオブジェクトを識別し、そのデータは含まれていないため、オブジェクトのすべてのインスタンスに固有の record キーがあります。 フォルダーおよびメッセージのレコードキーのスコープは、メッセージストアです。 アドレス帳コンテナー、メッセージングユーザー、および配布リストの範囲は、統合アドレス帳で使用するために MAPI によって提供されるトップレベルのコンテナーのセットです。
  
レコードキーは別のリソースに複製できます。 たとえば、2つの異なるメッセージストアの異なるメッセージは、同じ record キーを持つことができます。 これは、長期のエントリ識別子とは異なります。長期のエントリ識別子には、サービスプロバイダーへの参照が含まれているため、より広いスコープがあります。 メッセージストアの record キーは、スコープが長期のエントリ識別子に似ています。すべてのメッセージストアプロバイダーで一意である必要があります。 この一意性を確保するため、通常、メッセージストアプロバイダーは、 **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) プロパティと、メッセージストアに固有の識別子の組み合わせである値にレコードキーを設定します。
  
## <a name="search-keys"></a>検索キー

検索キーは、2つのオブジェクトのデータを比較するために使用されます。 オブジェクトの検索キーは、その**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティに格納されます。 検索キーはオブジェクトのデータを表し、オブジェクト自体ではないため、同じデータを持つ2つの異なるオブジェクトは同じ検索キーを持つことができます。 たとえば、オブジェクトがコピーされると、元のオブジェクトとそのコピーの両方に同じデータと同じ検索キーが設定されます。
  
メッセージおよびメッセージングユーザーには、検索キーがあります。 メッセージの検索キーは、メッセージのデータの一意の識別子です。 メッセージストアプロバイダーは、メッセージの作成時に、メッセージの**PR_SEARCH_KEY**プロパティを提供します。 アドレス帳エントリの検索キーは、アドレスの種類 (**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))) および address (**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))) から計算されます。 アドレス帳エントリが書き込み可能な場合、 [imapiprop:: setprops](imapiprop-setprops.md)メソッドを使用してアドレスの種類とアドレスが設定されていると、その検索キーが使用できなくなることがあります。このエントリは、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを使用して保存されています。 これらのアドレスのプロパティが変更された場合は、変更が**SaveChanges**呼び出しでコミットされるまで、対応する検索キーが新しい値と同期されないようにすることができます。 
  
オブジェクトの record キーの値は、サービスプロバイダーに応じて、検索キーの値と同じか異なることができます。 一部のサービスプロバイダーは、オブジェクトの検索キー、レコードキー、およびエントリ識別子に同じ値を使用します。 その他のサービスプロバイダーは、オブジェクトの識別子ごとに一意の値を割り当てます。 
  
## <a name="see-also"></a>関連項目



[MAPI アプリケーションの開発](mapi-application-development.md)

