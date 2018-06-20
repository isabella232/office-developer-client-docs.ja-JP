---
title: MAPI エントリの識別子
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 84c37696-da7a-42e0-b8c0-29658a6c9a48
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b8212f4a055125858b77ee615a5d929a4a62bb82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801353"
---
# <a name="mapi-entry-identifiers"></a>MAPI エントリの識別子

  
  
**適用されます**: Outlook 
  
エントリの識別子は、一意に識別し、MAPI オブジェクトを開くに使用される[エントリ ID](entryid.md)の構造体に格納されているバイナリのデータの一部です。 MAPI オブジェクトのほとんどは、エントリ id を持ちます。 オブジェクトのエントリ id は、ファイルのファイル名に似ています。 ただし、送信できる、できないに発生したシステム以外のシステムでは使用できません。 
  
## <a name="entry-identifiers"></a>エントリ Id

メッセージ ストア プロバイダーでは、エントリ id を割り当てるにメッセージ ・ ストア、フォルダー、およびメッセージです。アドレス帳プロバイダーでは、アドレス帳コンテナー、配布リスト、およびメッセージングのユーザーに割り当てます。 状態テーブル内の状態のオブジェクトなど、テーブル内の行によって表されるオブジェクトを開くには、エントリ id は使用されます。 オブジェクトは、それぞれのプロパティの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) でそれらのエントリの識別子を格納します。 
  
サービス ・ プロバイダーを作成、割り当て、およびエントリの識別子を調べて、クライアント アプリケーションとしてのみ使用してツールのオブジェクトを開くためです。 クライアントでは、エントリ id は、不透明なバイナリ データに基になるメッセージング システムとは無関係します。 
  
クライアントは、その**PR_ENTRYID**プロパティを取得するオブジェクトの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドまたは**PR_ENTRYID**プロパティを保持する列を取得するテーブルの[IMAPITable::QueryColumns](imapitable-querycolumns.md)メソッドを呼び出します。 
  
エントリ id は、 **OpenEntry**と**CompareEntryIDs**メソッドにパラメーターとして渡されます。 MAPI オブジェクトのいくつかは、 **OpenEntry**と**CompareEntryIDs**メソッドを実装します。 **OpenEntry**クライアントはオブジェクトを開くことができます。 **CompareEntryIDs**クライアントは同じオブジェクトを参照しているかどうかを決定する 2 つのエントリ id を比較できます。 エントリ id は必ずしもバイナリではないため同等で、クライアントする必要がありますそれらを比較、 **CompareEntryIDs**メソッドによって。 
  
クライアントは常に成功必然的に配置されたエントリの識別子でサービス ・ プロバイダーへの呼び出しが、サービス プロバイダーは、任意に調整されているエントリの識別子を処理する必要があります、これが常に大文字と小文字。 自然にアラインメントされたメモリ アドレスでは、整列エラーを生成することがなくそのアドレスをサポートしている任意のデータ型にアクセスするコンピューターを使用できます。 自然配列の要素は、通常、システムのメモリ アロケーターによって使用される同じ配置係数、通常 8 バイトです。
  
エントリの識別子には 2 つのタイプ: 短期および長期的な。 短期的なエントリ id は、構成する際、高速ですが、現在のセッションの現在のワークステーションの寿命を延ばす上でのみ、一意性が保証されます。 長期のエントリ id より長寿命があります。 短期的なエントリ id は、多くのオブジェクト、フォルダー、メッセージなどの長期のエントリ id を使用し、配布リストが、テーブル内の行と、ダイアログ ボックス内のエントリの主に使用されます。
  
## <a name="see-also"></a>関連項目



[MAPI �A�v���P�[�V�����̊J��](mapi-application-development.md)

