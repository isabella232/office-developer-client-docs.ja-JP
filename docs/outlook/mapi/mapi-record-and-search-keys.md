---
title: MAPI レコードと検索キー
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
# <a name="mapi-record-and-search-keys"></a>MAPI レコードと検索キー

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
レコード キーと検索キーは、多くの MAPI オブジェクトに割り当てられているバイナリ識別子です。 オブジェクトのエントリ識別子とは異なり、レコードまたは検索キーは直接同等で、送信可能です。 
  
## <a name="record-keys"></a>レコード キー

レコード キーを使用して、2 つのオブジェクトを比較します。 メッセージ ストア オブジェクトとアドレス帳オブジェクトには、レコード キーが必要です。このキーは、PR_RECORD_KEY **(** [PidTagRecordKey](pidtagrecordkey-canonical-property.md)) プロパティに格納されます。 レコード キーはオブジェクトを識別し、データを識別しないので、オブジェクトのすべてのインスタンスには一意のレコード キーがあります。 フォルダーとメッセージのレコード キーのスコープは、メッセージ ストアです。 アドレス帳コンテナー、メッセージング ユーザー、配布リストのスコープは、統合アドレス帳で使用するために MAPI によって提供される一連のトップ レベル のコンテナーです。
  
レコード キーは、別のリソースで複製できます。 たとえば、2 つの異なるメッセージ ストア内の異なるメッセージに同じレコード キーを設定できます。 これは、長期的なエントリ識別子とは異なります。長期エントリ識別子にはサービス プロバイダーへの参照が含まれているため、スコープが広くなります。 メッセージ ストアのレコード キーは、スコープ内で長期的なエントリ識別子と似ています。すべてのメッセージ ストア プロバイダーで一意である必要があります。 この一意性を確保するために、メッセージ ストア プロバイダーは通常、レコード キーを **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) プロパティとメッセージ ストアに固有の識別子の組み合わせの値に設定します。
  
## <a name="search-keys"></a>検索キー

検索キーは、2 つのオブジェクトのデータを比較するために使用されます。 オブジェクトの検索キーは、プロパティ ([PidTagSearchKey](pidtagsearchkey-canonical-property.md) **)** PR_SEARCH_KEYに格納されます。 検索キーはオブジェクト自体ではなくオブジェクトのデータを表すので、同じデータを持つ 2 つの異なるオブジェクトが同じ検索キーを持つ場合があります。 たとえば、オブジェクトをコピーすると、元のオブジェクトとコピーの両方に同じデータと同じ検索キーが設定されます。
  
メッセージとメッセージング ユーザーには検索キーがあります。 メッセージの検索キーは、メッセージのデータの一意の識別子です。 メッセージ ストア プロバイダーは、メッセージの作成時に **PR_SEARCH_KEYのプロパティ** を提供します。 アドレス帳エントリの検索キーは、そのアドレスの種類 (**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))) とアドレス ( PR_EMAIL_ADDRESS ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))) から計算されます。 アドレス帳エントリが書き込み可能な場合は [、IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを使用してアドレスの種類とアドレスが設定され [、IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを使用してエントリが保存されるまで、その検索キーを使用できない場合があります。 これらのアドレス プロパティが変更された場合 **、SaveChanges** 呼び出しで変更がコミットされるまで、対応する検索キーが新しい値と同期されない可能性があります。 
  
オブジェクトのレコード キーの値は、サービス プロバイダーに応じて、検索キーの値と同じか異なる場合があります。 一部のサービス プロバイダーは、オブジェクトの検索キー、レコード キー、およびエントリ識別子に同じ値を使用します。 他のサービス プロバイダーは、オブジェクトの識別子ごとに一意の値を割り当てる。 
  
## <a name="see-also"></a>関連項目



[MAPI アプリケーション開発](mapi-application-development.md)

