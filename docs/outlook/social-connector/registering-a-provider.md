---
title: プロバイダーの登録
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: このトピックでは、Outlook Social Connector (.osc) プロバイダーをインストールするときに使用される Windows レジストリの場所について説明します。
ms.openlocfilehash: a5f76850f9bebcba3c2bff31e799a3b012d6b91a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421761"
---
# <a name="registering-a-provider"></a>プロバイダーの登録

このトピックでは、Outlook Social Connector (.osc) プロバイダーをインストールするときに使用される Windows レジストリの場所について説明します。
  
## <a name="com-registration"></a>COM 登録

インストール時に COM の自己登録または regsvr32 を使用して登録するように、.osc プロバイダー DLL を構成する必要があります。 プロバイダー DLL の COM 登録は、 `HKEY_CLASSES_ROOT`レジストリハイブの下に、.osc プロバイダーを登録します。 
  
マネージコードで開発された .osc プロバイダには、COM で参照できるプロバイダアセンブリがあります。 プロバイダーコンポーネントには、別のアプリケーションドメインを使用する必要があります。 それ以外の場合、.osc プロバイダーは、他のコンポーネントで使用されている既定の共有アプリケーションドメインを使用しますが、プロバイダーは期待どおりに動作しない可能性があります。
  
## <a name="registering-provider-progid"></a>プロバイダー ProgID の登録

各 .osc プロバイダーは、プログラム id (`ProgID`) を登録する必要があります。 プロバイダーインストーラーは、次のいずれかの場所を選択して、 `ProgID`を追加または削除できます。
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash;プロバイダーのインストーラーは、プロバイダーが現在ログオンしているユーザーに対してのみインストールされている場合は、この場所を使用する必要があります。
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash;プロバイダーインストーラーは、プロバイダーがコンピューター上のすべてのユーザーに対してインストールされている場合に、この場所を使用する必要があります。
    
クライアントコンピューターに32ビットの`ProgID` Outlook が64ビットの Windows オペレーティングシステムで実行されている場合を除き、.osc は上記の場所でプロバイダーを探します。 このような場合`HKEY_CURRENT_USER`は、プロバイダーのインストーラーで、または`HKEY_LOCAL_MACHINE`ハイブに次のいずれかの場所を選択する必要があります。 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
クイック実行バージョンの Office の場合、プロバイダーのインストーラーは、HKEY_CURRENT_USER または HKEY_LOCAL_MACHINE ハイブの次のいずれかの場所を選択する必要があります。
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a>関連項目

- [インストールチェックリスト](installation-checklist.md)
- [プロバイダーを開発するための簡単な手順](quick-steps-for-learning-to-develop-a-provider.md)
- [プロバイダーを展開する](deploying-a-provider.md)

