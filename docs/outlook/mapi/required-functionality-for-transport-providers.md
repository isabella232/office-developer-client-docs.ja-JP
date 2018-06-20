---
title: トランスポート プロバイダーに必要な機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: eb5d70c31f28df16593fb020f13124ea217476ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803773"
---
# <a name="required-functionality-for-transport-providers"></a>トランスポート プロバイダーに必要な機能

  
  
**適用されます**: Outlook 
  
すべての MAPI トランスポート プロバイダーが必要です。
  
- MAPI およびその他のサービス プロバイダーを操作するための一般的なガイドラインに従います。 詳細については、 [MAPI アプリケーションの開発](mapi-application-development.md)と[サービスの MAPI プロバイダー](mapi-service-providers.md)を参照してください。
    
- トランスポート プロバイダーを MAPI DLL の公開、 [XPProviderInit](xpproviderinit.md)の初期化関数があります。 
    
- MAPI への実装を公開します[IXPProvider: IUnknown](ixpprovideriunknown.md)と[IXPLogon: IUnknown](ixplogoniunknown.md)インタ フェースです。 
    
- MAPI およびクライアント アプリケーションへの実装を公開します[IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)インタ フェースです。 **IMAPIStatus**の実装の詳細については、[状態オブジェクトの実装](status-object-implementation.md)を参照してください。 
    
- 構成のプロパティ シートのダイアログ ボックスを実装します。 プロパティ シートの実装の詳細については、[プロパティ シートの実装](property-sheet-implementation.md)を参照してください。
    

