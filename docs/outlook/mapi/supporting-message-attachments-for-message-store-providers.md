---
title: メッセージ ストア プロバイダーでのメッセージ添付ファイルのサポート
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d5fabc40-71e8-4afa-9846-533da605ce6c
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: a94d1230f4f26d080976fd15768bdfeb6ea04748
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576100"
---
# <a name="supporting-message-attachments-for-message-store-providers"></a>メッセージ ストア プロバイダーでのメッセージ添付ファイルのサポート

 
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージ ストア プロバイダーは、メッセージの添付ファイルをサポートする必要はありません。 ただし、多くのクライアント アプリケーションは、メッセージに添付ファイルを追加するのにはできるはずです。 作成または IPM を格納する場合は、メッセージ ・ ストアが使用されます。メッセージの添付ファイルをサポートする必要がありますし、メッセージに注意してください。 既定のメッセージ ストア プロバイダーは、メッセージの添付ファイルもサポートする必要があります。 詳細については、 [MAPI メッセージ クラス](mapi-message-classes.md)、および[既定のメッセージ ストア](default-message-stores.md)を参照してください。
  
MAPI をサポートしている添付ファイルの 5 種類があります: ファイルの添付ファイル、データの添付ファイル、メッセージの添付ファイル、OLE オブジェクトの添付ファイルとリンクします。 それぞれの種類をサポートするための要件は、異なります。 クライアントは、オブジェクトの添付ファイルの**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティを使用して添付ファイルの 2 種類を区別します。
  
添付ファイルのサポートを実装することを意味します[IAttach: IMAPIProp](iattachimapiprop.md)インタ フェースです。 **IAttach**インターフェイスには独自のメソッドがありません。[IMAPIProp](imapipropiunknown.md)インターフェイスから継承されたメソッドのみを備えています。 メッセージ ストア プロバイダーは、メッセージ オブジェクトのプロパティを実装する必要があります既にため、この大幅に簡略化タスクの添付ファイルをサポートします。 基本的に**IAttach**を実装すると、クライアントがメッセージの添付ファイルを特定のプロパティのテーブルにアクセスするための手段を提供することを意味します。 
  
データの添付ファイルは、添付ファイルの内容は、添付ファイルの**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) のプロパティに直接格納されている添付ファイルだけです。 データの添付ファイルは、クライアントが送信者とメッセージの受信者に共通のファイル ・ サーバへのアクセスがないときに、メッセージにファイルを添付できるようにするには、主に存在します。 詳細については、 **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) のプロパティを参照してください。
  
メッセージの添付ファイルは、添付ファイルの添付ファイルのサブオブジェクトの別[IMessage: MAPIProp](imessageimapiprop.md)オブジェクトです。 メッセージ ストア プロバイダーは、既に**IMessage**インターフェイスをサポートするので、メッセージの添付ファイルをサポートしている困難はありません。 
  
オブジェクトの OLE 添付ファイルをサポートしている OLE **IStorage**、 **IStream**を**IStreamDocfile**インターフェイスを実装することを意味します。 メッセージ ストア プロバイダーは、クライアントがオブジェクトを開いたときにアクティブな OLE オブジェクト、メッセージに格納されている OLE オブジェクトのデータに変換できる必要があります。 
  
リンクには 2 つの種類: ファイルおよびその他のメッセージへのリンクへのリンクです。 ファイルへのリンクでは、 **PR_ATTACH_METHOD**プロパティを**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) または**PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) およびの ATTACH_BY_REF_ONLY 値を使用してファイルの場所です。
  
メッセージへのリンクを実装するいずれかの方法ローカルのメッセージング システムの側面に依存している可能性があり、として次のようなことはできません完全に記述するここで。 リンクを送信するサーバー ベースのメッセージ ストアに保存されているメッセージには通常、送信者と受信者の両方があるそのサーバーへのアクセスを提供する、リンクされているメッセージのエントリ id を送信するだけで済みます。 他のメッセージング システムの構成では、他の要件とメッセージへのリンクを実装するための課題を提示します。
  
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

