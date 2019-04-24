---
title: メッセージストアプロバイダー用の構成インターフェイスの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c349a03b0be465ed1262712372b6ee17a9812abd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332978"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a>メッセージストアプロバイダー用の構成インターフェイスの実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストアプロバイダーは、ユーザーのコンピューター上で実行するようにメッセージストアプロバイダーを構成するためのインターフェイスを実装する必要があります。 通常、メッセージストアプロバイダーは、メッセージストアプロバイダーがユーザーのプロファイルに追加されたときに構成されます。 メッセージストアプロバイダーの構成インターフェイスは、一般的に、保護されたメッセージストアのユーザー名とパスワードの設定、必要なファイルへのパスの選択、必要に応じた基礎となるストレージメカニズムの作成などのタスクを処理します。
  
実装する構成インターフェイスは、メッセージサービスプロバイダーの DLL の追加エントリポイントを通じてアクセスされます。 詳細については、「[メッセージサービスを構成](configuring-a-message-service.md)する」を参照してください。 メッセージストアプロバイダーの構成インターフェイスは、メッセージストアプロバイダーが実装する必要がある唯一のユーザーインターフェイスです。
  
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

