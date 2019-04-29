---
title: メッセージストアプロバイダーの必須およびオプションのインターフェイス
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc62e57e-82a4-4f37-8d1b-7cdf828b951e
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: 35b1d05d742b0d8defabf84b6dbf7d418ece0bbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420921"
---
# <a name="required-and-optional-interfaces-for-message-store-providers"></a>メッセージストアプロバイダーの必須およびオプションのインターフェイス

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI は、メッセージストアプロバイダーに関連する一連のインターフェイスを定義します。 メッセージストアで実装できるさまざまな機能があるため、これらのインターフェイスの一部は必須であり、一部は必要ありません。 次の表は、メッセージストアプロバイダーに関連する MAPI インターフェイスを示しています。インターフェイスが必須であるかオプションであるかを指定し、その目的について説明します。
  
|**インターフェイス**|**状態**|**説明**|
|:-----|:-----|:-----|
|[IMSProvider](imsprovideriunknown.md) <br/> |必須  <br/> |メッセージストアへのログオンとログオフを行います。  <br/> |
|[IMSLogon](imslogoniunknown.md) <br/> |必須  <br/> |フォルダーまたはメッセージを開き、メッセージストアの id を確認し、通知を処理します。  <br/> |
|[IMsgStore](imsgstoreimapiprop.md) <br/> |必須  <br/> |フォルダーまたはメッセージを開き、特別なフォルダーを検索し、メッセージの送信を処理します。  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |必須  <br/> |メッセージとサブフォルダーを検索して操作します。  <br/> |
|[IMessage](imessageimapiprop.md) <br/> |必須  <br/> |添付ファイルを操作し、一部のメッセージのプロパティを設定します。  <br/> |
|[IMAPITable](imapitableiunknown.md) <br/> |必須  <br/> |他のオブジェクトが、さまざまな MAPI コンポーネントにデータのコレクションを表示できるようにします。  <br/> |
|[IMAPIStatus](imapistatusimapiprop.md) <br/> |必須  <br/> |クライアントがメッセージストアの状態を検証し、いくつかの構成タスクを実行できるようにします。  <br/> |
|[iattach](iattachimapiprop.md) <br/> |省略可能  <br/> |ストアプロバイダーが添付ファイルをサポートしている場合は、メッセージ添付ファイルのプロパティにアクセスします。  <br/> |
|**IStorage** <br/> |省略可能  <br/> |ストアプロバイダーが OLE オブジェクトの添付ファイルをサポートしている場合は、構造化ストレージオブジェクトを管理します。  <br/> |
|**IStream** <br/> |省略可能  <br/> |メッセージおよび添付ファイルオブジェクトが、stream オブジェクトへのデータの読み取りおよび書き込みを行うことができるようにします。  <br/> |
|**IStreamDocfile** <br/> |省略可能  <br/> |一部のサービスプロバイダーが、OLE 2.0 ファイル形式の複合ファイルなどのストレージオブジェクトを開くことができるようにします。  <br/> |
   
**imapifolder**、 **IMessage**、 **imapifolder**、および**IMAPITable**を実装するために必要な基本情報については、これらのインターフェイスのリファレンストピックに記載されています。 このセクションには、メッセージストアプロバイダーに直接関連する補足情報が記載されています。 その他の MAPI インターフェイスは、このセクションの情報と適切な参照トピックに従って実装する必要があります。 **IStorage**、 **IStream**、および**IStreamDocFile**の実装の詳細については、「Windows SDK の COM および ActiveX のオブジェクトサービス」セクションを参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI メッセージ ストア プロバイダーの開発](developing-a-mapi-message-store-provider.md)

