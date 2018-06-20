---
title: MAPI の記録と検索キー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: caa7b7f3-a5a1-4f07-98c9-22652ecd5d21
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1e1b05be64029f80ec8a7379ed7b313b9cf645fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801431"
---
# <a name="mapi-record-and-search-keys"></a>MAPI の記録と検索キー

  
  
**適用されます**: Outlook 
  
レコードのキーとキーの検索は、多くの MAPI オブジェクトに割り当てられているバイナリの識別子です。 オブジェクトのエントリの識別子とは異なり、レコードまたは検索キーが直接比較できると同様に送信できます。 
  
## <a name="record-keys"></a>レコード キー

レコードのキーを使用して、2 つのオブジェクトを比較できます。 メッセージ ストアとアドレス帳オブジェクトには、 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) のプロパティに格納されるレコードのキーが必要があります。 オブジェクトとそのデータではなく、レコードのキーが識別されるため、オブジェクトのすべてのインスタンスは一意のレコード キーを持ちます。 フォルダーとメッセージのレコードのキーのスコープは、メッセージ ・ ストアです。 アドレス帳コンテナー、メッセージング ユーザー、および配布リストのスコープは、一連の統合のアドレス帳で使用するため、MAPI によって提供される最上位のコンテナーです。
  
別のリソースでは、レコードのキーを複製できます。 などの 2 つの別のメッセージ ストア内の別のメッセージは、同じレコードのキーを持つことができます。 これとは異なる長期的なエントリの識別子です。長期のエントリ id には、サービス プロバイダーへの参照が含まれている、のでより広い範囲があります。 メッセージ ストアのレコードのキーは、ようなスコープ内に長期のエントリ id です。メッセージ ストアのすべてのプロバイダー間で一意である必要があります。 この一意性を確保するには、メッセージ ストア プロバイダーは通常、 **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) のプロパティは、メッセージ ・ ストアに一意な識別子の組み合わせの値をそれらのレコードのキーを設定します。
  
## <a name="search-keys"></a>検索キー

検索キーを使用して、2 つのオブジェクト内のデータを比較できます。 **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティに、オブジェクトの検索キーが格納されます。 検索キーを表すため、オブジェクトのデータとオブジェクト自体ではなく、同じデータを持つ 2 つのオブジェクトは、同じ検索キーを持つことができます。 オブジェクトをコピーすると、たとえば、元のオブジェクトとそのコピーの両方がある同じデータと同一の検索キー。
  
メッセージおよびメッセージングのユーザーは、検索キーを持っています。 メッセージの検索キーは、メッセージのデータの一意な識別子です。 メッセージ ストア プロバイダーは、メッセージの作成時にメッセージの**PR_SEARCH_KEY**プロパティを提供します。 アドレス帳エントリの検索キーは、そのアドレスの種類 (**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))) とアドレス (**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))) から計算されます。 アドレス帳のエントリが書き込み可能な場合は、その検索キーできない可能性がありますまで、アドレスの種類とアドレスは、 [IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを使用して設定されているし、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを使用して、エントリが保存されました。 これらのアドレスのプロパティを変更する場合は、 **SaveChanges**の呼び出しでコミットされた変更しないと、新しい値を使用して同期に対応する検索キー可能性があります。 
  
オブジェクトのレコードのキーの値と同じか、サービス プロバイダーによって、検索キーの値と異なることができます。 サービス プロバイダーによっては、オブジェクトの検索キーをレコードのキーとエントリ id の同じ値を使用します。 その他のサービス プロバイダーは、そのオブジェクトの識別子の一意の値を割り当てます。 
  
## <a name="see-also"></a>関連項目



[MAPI �A�v���P�[�V�����̊J��](mapi-application-development.md)

