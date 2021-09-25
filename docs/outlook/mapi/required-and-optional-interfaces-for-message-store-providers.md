---
title: メッセージ ストア プロバイダーの必須インターフェイスと省略可能なインターフェイス
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: cc62e57e-82a4-4f37-8d1b-7cdf828b951e
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: 15937321d1f082f93413f541daa40e7bdb4e8f80
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578810"
---
# <a name="required-and-optional-interfaces-for-message-store-providers"></a>メッセージ ストア プロバイダーの必須インターフェイスと省略可能なインターフェイス

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI は、メッセージ ストア プロバイダーに関連する一連のインターフェイスを定義します。 メッセージ ストアで実装できる機能の範囲が広いので、これらのインターフェイスの一部は必須であり、一部は実装されません。 次の表に、メッセージ ストア プロバイダーに関連する MAPI インターフェイス、インターフェイスが必須か省略可能かを指定し、その目的を説明します。
  
|**インターフェイス**|**状態**|**説明**|
|:-----|:-----|:-----|
|[IMSProvider](imsprovideriunknown.md) <br/> |必須かどうか  <br/> |メッセージ ストアのログオンとオフを切り替えます。  <br/> |
|[IMSLogon](imslogoniunknown.md) <br/> |必須かどうか  <br/> |フォルダーまたはメッセージを開き、メッセージ ストアの ID を確認し、通知を処理します。  <br/> |
|[IMsgStore](imsgstoreimapiprop.md) <br/> |必須かどうか  <br/> |フォルダーまたはメッセージを開き、特別なフォルダーを検索し、メッセージの送信を処理します。  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |必須かどうか  <br/> |メッセージとサブフォルダーを検索および操作します。  <br/> |
|[IMessage](imessageimapiprop.md) <br/> |必須かどうか  <br/> |添付ファイルを操作し、メッセージのプロパティの一部を設定します。  <br/> |
|[IMAPITable](imapitableiunknown.md) <br/> |必須かどうか  <br/> |他のオブジェクトがさまざまな MAPI コンポーネントにデータのコレクションを表示できます。  <br/> |
|[IMAPIStatus](imapistatusimapiprop.md) <br/> |必須かどうか  <br/> |クライアントがメッセージ ストアの状態を検証し、いくつかの構成タスクを実行できます。  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |オプション  <br/> |ストア プロバイダーが添付ファイルをサポートしている場合は、メッセージ添付ファイルのプロパティにアクセスします。  <br/> |
|**IStorage** <br/> |オプション  <br/> |ストア プロバイダーが OLE オブジェクトの添付ファイルをサポートしている場合は、構造化ストレージ オブジェクトを管理します。  <br/> |
|**IStream** <br/> |オプション  <br/> |メッセージ オブジェクトと添付ファイル オブジェクトで、ストリーム オブジェクトへのデータの読み取りおよび書き込みを有効にできます。  <br/> |
|**IStreamDocfile** <br/> |オプション  <br/> |一部のサービス プロバイダーは、OLE 2.0 ファイル形式の複合ファイルなど、ストレージ オブジェクトを開きます。  <br/> |
   
IMAPIFolder、IMessage、IMAPIStatus、および **IMAPITable** を実装するために必要な基本情報は、これらのインターフェイスのリファレンス トピックに記載されています。  このセクションには、メッセージ ストア プロバイダーに直接関連する補足情報が含まれている。 MAPI インターフェイスの残りの部分は、このセクションの情報と適切な参照トピックに従って実装する必要があります。 **IStorage、IStream、** および **IStreamDocFile** の実装の詳細については、Windows SDK の COMおよび ActiveX オブジェクト サービス セクションを参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI メッセージ ストア プロバイダーの開発](developing-a-mapi-message-store-provider.md)

