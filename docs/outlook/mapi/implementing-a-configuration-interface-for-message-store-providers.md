---
title: メッセージ ストア プロバイダーの構成インターフェイスの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c349a03b0be465ed1262712372b6ee17a9812abd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415888"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a>メッセージ ストア プロバイダーの構成インターフェイスの実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストア プロバイダーは、ユーザーがメッセージ ストア プロバイダーを構成してそのユーザーのコンピューターで実行できるインターフェイスを実装する必要があります。 通常、メッセージ ストア プロバイダーは、メッセージ ストア プロバイダーがユーザーのプロファイルに追加される場合に構成されます。 メッセージ ストア プロバイダーの構成インターフェイスは、通常、保護されたメッセージ ストアのユーザー名とパスワードの設定、必要なファイルへのパスの選択、必要に応じて使用する基になるストレージ メカニズムの作成などのタスクを処理します。
  
実装する構成インターフェイスには、メッセージ サービス プロバイダーの DLL 内の追加のエントリ ポイントからアクセスします。 詳細については、「メッセージ サービス [の構成」を参照してください](configuring-a-message-service.md)。 メッセージ ストア プロバイダーの構成インターフェイスは、メッセージ ストア プロバイダーが実装する必要がある唯一のユーザー インターフェイスです。
  
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

