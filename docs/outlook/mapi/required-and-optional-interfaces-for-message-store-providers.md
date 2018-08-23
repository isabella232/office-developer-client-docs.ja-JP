---
title: メッセージ ストア プロバイダーの必須インターフェイスおよびオプションのインターフェイス
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc62e57e-82a4-4f37-8d1b-7cdf828b951e
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: 3305aaadbcf7d53b801ddaf7e31a0d63145fc7ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586964"
---
# <a name="required-and-optional-interfaces-for-message-store-providers"></a>メッセージ ストア プロバイダーの必須インターフェイスおよびオプションのインターフェイス

 
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI は、メッセージ ストア プロバイダーに関連するインターフェイスのセットを定義します。 により、広範囲の機能を実装するのには、メッセージ ・ ストアを選択できますが、これらのインタ フェースの一部と必要のいくつかです。 次の表は、メッセージ ストア プロバイダーに関連する MAPI インターフェイスを一覧表示、インターフェイスが必須またはオプションでは、およびその目的を説明かどうかを指定します。
  
|**インターフェイス**|**Status**|**説明**|
|:-----|:-----|:-----|
|[IMSProvider](imsprovideriunknown.md) <br/> |必須  <br/> |メッセージ ・ ストアのログです。  <br/> |
|[IMSLogon](imslogoniunknown.md) <br/> |必須  <br/> |フォルダーまたはメッセージが表示、メッセージ ストアの id を確認し、通知を処理します。  <br/> |
|[IMsgStore](imsgstoreimapiprop.md) <br/> |必須  <br/> |フォルダーまたはメッセージを開きます、特別なフォルダーを検索し、メッセージの送信を処理します。  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |必須  <br/> |検索し、メッセージとサブフォルダーを操作します。  <br/> |
|[IMessage](imessageimapiprop.md) <br/> |必須  <br/> |添付ファイルを操作し、いくつかのメッセージのプロパティを設定します。  <br/> |
|[IMAPITable](imapitableiunknown.md) <br/> |必須  <br/> |MAPI のさまざまなコンポーネントへのデータのコレクションを表示するには、他のオブジェクトを使用できます。  <br/> |
|[IMAPIStatus](imapistatusimapiprop.md) <br/> |必須  <br/> |メッセージ ストアの状態を検証していくつかの構成タスクを実行するクライアントを有効にします。  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |省略可能  <br/> |ストア プロバイダーは、ファイルの添付ファイルをサポートしている場合に、メッセージの添付ファイルのプロパティをアクセスします。  <br/> |
|**IStorage** <br/> |省略可能  <br/> |ストア プロバイダーは、OLE オブジェクトの添付ファイルをサポートしている場合は、構造化ストレージ オブジェクトを管理します。  <br/> |
|**IStream** <br/> |省略可能  <br/> |ストリーム オブジェクトにデータを読み書きするためのメッセージと添付ファイルのオブジェクトを使用できます。  <br/> |
|**IStreamDocfile** <br/> |省略可能  <br/> |開くには、記憶域オブジェクト、OLE 2.0 のファイル形式で複合ファイルなどの一部のサービス プロバイダーを使用できます。  <br/> |
   
**IMessage**、 **IMAPIFolder**、 **IMAPIStatus**、および**IMAPITable**を実装する必要が基本的な情報は、これらのインタ フェースのリファレンス トピックに記載されています。 このセクションには、メッセージ ストア プロバイダーに直接関連する補足情報が含まれています。 情報このセクションで、該当するリファレンス トピックに MAPI インターフェイスの残りの部分を実装する必要があります。 **IStorage**、 **IStream**、および**IStreamDocFile**の実装の詳細については Windows SDK の COM および ActiveX オブジェクト サービスのセクションを参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI ���b�Z�[�W �X�g�A �v���o�C�_�[�̊J��](developing-a-mapi-message-store-provider.md)

