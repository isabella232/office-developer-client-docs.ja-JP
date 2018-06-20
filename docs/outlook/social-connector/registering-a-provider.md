---
title: プロバイダーを登録します。
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: このトピックでは、Outlook ソーシャル コネクタ (OSC) プロバイダーをインストールするときに使用される Windows のレジストリの場所について説明します。
ms.openlocfilehash: 3ec594ec94b045d2ceb583144781a5746b945b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804452"
---
# <a name="registering-a-provider"></a>プロバイダーを登録します。

このトピックでは、Outlook ソーシャル コネクタ (OSC) プロバイダーをインストールするときに使用される Windows のレジストリの場所について説明します。
  
## <a name="com-registration"></a>COM の登録

OSC プロバイダーのインストール中に、COM 登録または regsvr32 を使用して登録するのには DLL を構成する必要があります。 OSC プロバイダーを登録するプロバイダーの DLL の COM 登録、`HKEY_CLASSES_ROOT`のレジストリ ハイブです。 
  
OSC プロバイダーがマネージ コードで開発されたは、プロバイダー アセンブリを COM 参照可能です。 プロバイダー コンポーネントの個別のアプリケーション ドメインを使用してください。 それ以外の場合、OSC プロバイダーは、他のコンポーネントによって使用される既定の共有のアプリケーション ドメインを使用し、期待どおりに、プロバイダーが動作しない可能性があります。
  
## <a name="registering-provider-progid"></a>プロバイダーの ProgID を登録します。

各 OSC プロバイダーは、プログラム識別子を登録する必要があります (`ProgID`)。 プロバイダーのインストーラーは、次の場所を追加または削除のいずれかを選択できます、 `ProgID`。
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash;プロバイダーが現在ログオンしているユーザーだけにインストールされている場合に、プロバイダーのインストーラーがこの場所を使用する必要があります。
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash;プロバイダーは、コンピューター上のすべてのユーザーに対してインストールされている場合に、プロバイダーのインストーラーがこの場所を使用する必要があります。
    
OSC プロバイダーの次の`ProgID`で上記の場所では、クライアント コンピューターは、64 ビット Windows オペレーティング システムで実行されている 32 ビットの Outlook を持っていない限り、します。 このような場合は、プロバイダー インストーラーする必要がありますを選択して次の場所のいずれか、`HKEY_CURRENT_USER`または`HKEY_LOCAL_MACHINE`ハイブ。 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
クイック実行バージョンの Office には、プロバイダー インストーラーする必要がありますを選択して次の場所のいずれかの HKEY_CURRENT_USER または HKEY_LOCAL_MACHINE ハイブに。
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a>関連項目

- [インストールのチェックリスト](installation-checklist.md)
- [プロバイダーを開発する学習のためのクイック ステップ](quick-steps-for-learning-to-develop-a-provider.md)
- [プロバイダーを展開します。](deploying-a-provider.md)

