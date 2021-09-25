---
title: メッセージ ストア プロバイダーの構成インターフェイスの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 56ef4e25ad432acc42959aa1b6034ad0c02add31
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575653"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a>メッセージ ストア プロバイダーの構成インターフェイスの実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストア プロバイダーは、ユーザーがメッセージ ストア プロバイダーを構成してそのユーザーのコンピューターで実行できるインターフェイスを実装する必要があります。 通常、メッセージ ストア プロバイダーは、メッセージ ストア プロバイダーがユーザーのプロファイルに追加される場合に構成されます。 メッセージ ストア プロバイダーの構成インターフェイスは、通常、保護されたメッセージ ストアのユーザー名とパスワードの設定、必要なファイルへのパスの選択、必要に応じて使用する基になるストレージ メカニズムの作成などのタスクを処理します。
  
実装する構成インターフェイスには、メッセージ サービス プロバイダーの DLL 内の追加のエントリ ポイントからアクセスします。 詳細については、「メッセージ サービス [の構成」を参照してください](configuring-a-message-service.md)。 メッセージ ストア プロバイダーの構成インターフェイスは、メッセージ ストア プロバイダーが実装する必要がある唯一のユーザー インターフェイスです。
  
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

