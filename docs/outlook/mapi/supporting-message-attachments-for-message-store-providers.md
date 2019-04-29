---
title: メッセージストアプロバイダーのメッセージ添付ファイルのサポート
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d5fabc40-71e8-4afa-9846-533da605ce6c
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: 69d1df5bf206cddd0d25698665c9fd87b81e4ea5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412136"
---
# <a name="supporting-message-attachments-for-message-store-providers"></a>メッセージストアプロバイダーのメッセージ添付ファイルのサポート

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストアプロバイダーは、メッセージの添付ファイルをサポートする必要はありません。 ただし、多くのクライアントアプリケーションでは、メッセージに添付ファイルを追加できることが想定されています。 メッセージストアを使用して、IPM を作成または保存する場合。メッセージを確認してから、メッセージの添付ファイルをサポートする必要があります。 既定のメッセージストアプロバイダーは、メッセージの添付ファイルもサポートする必要があります。 詳細については、「 [MAPI メッセージクラス](mapi-message-classes.md)」および「[既定のメッセージストア](default-message-stores.md)」を参照してください。
  
MAPI がサポートする添付ファイルには、添付ファイル、データ添付ファイル、メッセージの添付ファイル、OLE オブジェクトの添付ファイル、リンクの5種類があります。 各種類をサポートするための要件は異なります。 クライアントは、attachment オブジェクトの**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティを使って、2種類の添付ファイルを区別します。
  
添付ファイルのサポートとは、 [iattach: imapiprop](iattachimapiprop.md)インターフェイスを実装することを意味します。 **iattach**インターフェイスには、独自のメソッドはありません。[imapiprop](imapipropiunknown.md)インターフェイスから継承されたメソッドのみが含まれています。 メッセージストアプロバイダーは、既にメッセージオブジェクトのプロパティを実装している必要があるので、これにより、添付ファイルをサポートするタスクが大幅に簡略化されます。 **iattach**の実装は基本的に、クライアントがメッセージの特定の添付ファイルのプロパティのテーブルにアクセスする方法を提供することを意味します。 
  
データの添付ファイルは、添付ファイルの内容が添付ファイルの**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) プロパティに直接格納される添付ファイルです。 データの添付ファイルは主に、メッセージの送信者と受信者が共通のファイルサーバーにアクセスできない場合に、クライアントがメッセージにファイルを添付できるようにすることを目的としています。 詳細については、 **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティを参照してください。
  
メッセージの添付ファイルは、添付ファイルサブオブジェクトが別の[IMessage: MAPIProp](imessageimapiprop.md)オブジェクトである添付ファイルです。 メッセージストアプロバイダーは**IMessage**インターフェイスを既にサポートしているため、メッセージの添付ファイルをサポートするのは困難ではありません。 
  
ole オブジェクトの添付ファイルをサポートすることは、ole **IStorage**、 **IStream**、および**IStreamDocfile**インターフェイスを実装することを意味します。 クライアントがオブジェクトを開いたとき、メッセージストアプロバイダーは、メッセージに格納されている ole オブジェクトデータをアクティブな ole オブジェクトに変換できる必要があります。 
  
リンクには、ファイルへのリンクと他のメッセージへのリンクの2種類があります。 ファイルへのリンク**PR_ATTACH_METHOD**プロパティの ATTACH_BY_REF_ONLY 値を**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) または**PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) と共に使用して指定します。ファイルの場所を指定します。
  
メッセージへのリンクを実装する方法は、ローカルメッセージングシステムの機能によって異なる場合があります。そのため、ここでは完全にドキュメント化することはできません。 たとえば、サーバーベースのメッセージストアに格納されているメッセージにリンクを送信する場合は、通常、リンクされたメッセージのエントリ識別子を送信するだけで、送信者と受信者の両方がそのサーバーにアクセスできるようになります。 他のメッセージングシステム構成には、メッセージへのリンクの実装に関するその他の要件および課題があります。
  
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

