---
title: メッセージ ストア プロバイダー用の構成インターフェイスの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 15833768fbd148ae4e689b5a80ed3479823864cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592928"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a>メッセージ ストア プロバイダー用の構成インターフェイスの実装

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージ ストア プロバイダーは、そのユーザーのコンピューター上で実行するメッセージ ストア プロバイダーを構成するユーザーをできるようにするインターフェイスを実装する必要があります。 通常、メッセージ ストア プロバイダーは、ユーザーのプロファイルに追加するときに、メッセージ ストア プロバイダーが構成されます。 メッセージ ストア プロバイダーの構成インターフェイスは一般にユーザー名とパスワードに必要なファイルへのパスを選択する、保護されたメッセージ ストアを設定するなどのタスクを処理し、基になるストレージ機構を作成するには、必要に応じて使用します。
  
構成インターフェイスを実装するは、メッセージ サービス プロバイダーの DLL 内の他のエントリ ポイントを通じてアクセスされます。 詳細については、[メッセージ サービスの構成](configuring-a-message-service.md)を参照してください。 メッセージ ストア プロバイダーの構成のインターフェイスは、メッセージ ストア プロバイダーを実装する必要があります唯一のユーザー インターフェイスです。
  
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

