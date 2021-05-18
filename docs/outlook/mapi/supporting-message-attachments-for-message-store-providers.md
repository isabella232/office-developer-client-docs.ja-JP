---
title: メッセージ ストア プロバイダーのメッセージ添付ファイルのサポート
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
# <a name="supporting-message-attachments-for-message-store-providers"></a>メッセージ ストア プロバイダーのメッセージ添付ファイルのサポート

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストア プロバイダーがメッセージの添付ファイルをサポートする必要はない。 ただし、多くのクライアント アプリケーションでは、メッセージに添付ファイルを追加できると予想されます。 メッセージ ストアを使用して IPM を作成または保存する場合。メッセージをメモし、メッセージの添付ファイルをサポートする必要があります。 既定のメッセージ ストア プロバイダーは、メッセージの添付ファイルもサポートする必要があります。 詳細については、「MAPI メッセージ [クラス」および「](mapi-message-classes.md)既定 [のメッセージ ストア」を参照してください](default-message-stores.md)。
  
MAPI でサポートされる添付ファイルには、ファイル添付ファイル、データ添付ファイル、メッセージ添付ファイル、OLE オブジェクト添付ファイル、およびリンクの 5 種類があります。 各種類をサポートするための要件は異なります。 クライアントは、添付ファイル オブジェクトの PR_ATTACH_METHOD **(** [PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティを使用して、2 種類の添付ファイルを区別します。
  
添付ファイルのサポートとは [、IAttach : IMAPIProp インターフェイスの実装を意味](iattachimapiprop.md) します。 **IAttach インターフェイス** には、独自のメソッドはありません。[IMAPIProp](imapipropiunknown.md)インターフェイスから継承されるメソッドだけが存在します。 メッセージ ストア プロバイダーは既にメッセージ オブジェクトのプロパティを実装する必要があります。これにより、添付ファイルのサポートタスクが大幅に簡素化されます。 **IAttach を実装する** ということは、基本的には、クライアントがメッセージの特定の添付ファイルのプロパティ テーブルにアクセスする方法を提供する手段を提供します。 
  
データ添付ファイルは、添付ファイルの内容が添付ファイルのプロパティ **(** [PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) プロパティに直接格納PR_ATTACH_DATA_BIN添付ファイルです。 データ添付ファイルは、主に、メッセージの送信者と受信者が共通のファイル サーバーにアクセスできない場合に、クライアントがメッセージにファイルを添付するために存在します。 詳細については、「PR_ATTACH_METHOD **(** [PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティ」を参照してください。
  
メッセージの添付ファイルは、添付ファイルサブオブジェクトが別の [IMessage : MAPIProp オブジェクトである添付ファイル](imessageimapiprop.md) です。 メッセージ ストア プロバイダーは既に **IMessage** インターフェイスをサポートしています。メッセージの添付ファイルをサポートすることは困難ではありません。 
  
OLE オブジェクトの添付ファイルのサポートとは、OLE **IStorage、IStream、****および IStreamDocfile インターフェイスを実装する方法** を意味します。  メッセージ ストア プロバイダーは、クライアントがオブジェクトを開くと、メッセージに格納されている OLE オブジェクト データをアクティブな OLE オブジェクトに変換できる必要があります。 
  
リンクには、ファイルへのリンクと他のメッセージへのリンクの 2 種類があります。 ファイルへのリンクでは **、PR_ATTACH_METHOD** プロパティの ATTACH_BY_REF_ONLY 値と PR_ATTACH_PATHNAME ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) または **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) を使用して、ファイルの場所を指定します。 
  
メッセージへのリンクを実装する方法は、ローカル メッセージング システムの側面によって異なる場合があります。そのため、ここでは完全に文書化できません。 たとえば、サーバー ベースのメッセージ ストアに格納されているメッセージへのリンクの送信は、通常、リンクされたメッセージのエントリ識別子を送信し、送信者と受信者の両方がサーバーにアクセスできるだけの問題です。 他のメッセージング システム構成では、メッセージへのリンクを実装するためのその他の要件と課題が示されています。
  
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

