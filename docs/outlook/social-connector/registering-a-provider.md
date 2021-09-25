---
title: プロバイダーの登録
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: このトピックでは、Windows ソーシャル コネクタ (OSC) プロバイダーのインストール時に使用Outlookレジストリの場所について説明します。
ms.openlocfilehash: 78f5b102cc5ec50e334aafa4a5fef10c37fa2953
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604056"
---
# <a name="registering-a-provider"></a>プロバイダーの登録

このトピックでは、Windows ソーシャル コネクタ (OSC) プロバイダーのインストール時に使用Outlookレジストリの場所について説明します。
  
## <a name="com-registration"></a>COM 登録

インストール時に COM 自己登録または regsvr32 を使用して登録する OSC プロバイダー DLL を構成する必要があります。 プロバイダー DLL の COM 登録は、レジストリ ハイブの下に OSC `HKEY_CLASSES_ROOT` プロバイダーを登録します。 
  
マネージ コードで開発された OSC プロバイダーには、COM に表示されるプロバイダー アセンブリがあります。 プロバイダー コンポーネントには、別のアプリケーション ドメインを使用する必要があります。 それ以外の場合、OSC プロバイダーは、他のコンポーネントで使用される既定の共有アプリケーション ドメインを使用し、プロバイダーが期待した通りに動作しない可能性があります。
  
## <a name="registering-provider-progid"></a>プロバイダー ProgID の登録

各 OSC プロバイダーは、プログラム識別子 () を登録する必要があります `ProgID` 。 プロバイダー インストーラーは、次のいずれかの場所を選択して、次の場所を追加または削除できます `ProgID` 。
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`プロバイダーが現在ログオンしているユーザーにのみインストールされている場合は、プロバイダーインストーラーでこの &ndash; 場所を使用する必要があります。
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash;プロバイダーインストーラーは、プロバイダーがコンピューター上のすべてのユーザーにインストールされている場合、この場所を使用する必要があります。
    
OSC は、クライアント コンピューターが 64 ビット オペレーティング システムで 32 ビット Outlookを実行している場合をWindows `ProgID` します。 このような場合、プロバイダー インストーラーは、次のいずれかの場所またはハイブ内の場所  `HKEY_CURRENT_USER` を選択する必要  `HKEY_LOCAL_MACHINE` があります。 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
バージョン 1 クイック実行の場合Officeプロバイダー インストーラーは、次のいずれかの場所を選択する必要があります。HKEY_CURRENT_USERまたはHKEY_LOCAL_MACHINEします。
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a>関連項目

- [インストール チェックリスト](installation-checklist.md)
- [プロバイダーを開発するためのラーニング手順](quick-steps-for-learning-to-develop-a-provider.md)
- [プロバイダーの展開](deploying-a-provider.md)

