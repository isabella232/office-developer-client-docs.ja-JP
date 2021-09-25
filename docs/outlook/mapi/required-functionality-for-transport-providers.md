---
title: トランスポート プロバイダーに必要な機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b08057ce597459988fc443f5e7495b45fdef56a7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578796"
---
# <a name="required-functionality-for-transport-providers"></a>トランスポート プロバイダーに必要な機能

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
すべての MAPI トランスポート プロバイダーは、次の必要があります。
  
- MAPI および他のサービス プロバイダーの操作に関する一般的なガイドラインに従います。 詳細については [、「MAPI アプリケーション開発と](mapi-application-development.md) [MAPI サービス プロバイダー」を参照してください](mapi-service-providers.md)。
    
- トランスポート プロバイダー DLL を MAPI の [XPProviderInit 初期化関数に](xpproviderinit.md) 公開します。 
    
- [IXPProvider : IUnknown](ixpprovideriunknown.md)と[IXPLogon : IUnknown](ixplogoniunknown.md)インターフェイスの実装を MAPI に公開します。 
    
- MAPI およびクライアント アプリケーションに対して [IMAPIStatus : IMAPIProp インターフェイスの実装を公開](imapistatusimapiprop.md) します。 **IMAPIStatus** の実装の詳細については、「Status Object Implementation [」を参照してください](status-object-implementation.md)。 
    
- 構成用のプロパティ シート ダイアログ ボックスを実装します。 プロパティ シートの実装の詳細については、「プロパティ シートの [実装」を参照してください](property-sheet-implementation.md)。
    

