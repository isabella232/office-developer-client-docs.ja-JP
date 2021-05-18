---
title: トランスポート プロバイダーに必要な機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7f9768d47cf740bdf50b439ee3af4b0d2a191602
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404443"
---
# <a name="required-functionality-for-transport-providers"></a>トランスポート プロバイダーに必要な機能

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
すべての MAPI トランスポート プロバイダーは、次の必要があります。
  
- MAPI および他のサービス プロバイダーの操作に関する一般的なガイドラインに従います。 詳細については [、「MAPI アプリケーション開発と](mapi-application-development.md) [MAPI サービス プロバイダー」を参照してください](mapi-service-providers.md)。
    
- トランスポート プロバイダー DLL を MAPI の [XPProviderInit 初期化関数に](xpproviderinit.md) 公開します。 
    
- [IXPProvider : IUnknown](ixpprovideriunknown.md)と[IXPLogon : IUnknown](ixplogoniunknown.md)インターフェイスの実装を MAPI に公開します。 
    
- MAPI およびクライアント アプリケーションに対して [IMAPIStatus : IMAPIProp インターフェイスの実装を公開](imapistatusimapiprop.md) します。 **IMAPIStatus** の実装の詳細については、「Status Object Implementation [」を参照してください](status-object-implementation.md)。 
    
- 構成用のプロパティ シート ダイアログ ボックスを実装します。 プロパティ シートの実装の詳細については、「プロパティ シートの [実装」を参照してください](property-sheet-implementation.md)。
    

