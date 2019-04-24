---
title: トランスポートプロバイダーに必要な機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7f9768d47cf740bdf50b439ee3af4b0d2a191602
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328687"
---
# <a name="required-functionality-for-transport-providers"></a>トランスポートプロバイダーに必要な機能

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
すべての MAPI トランスポートプロバイダーは次のことを行う必要があります。
  
- MAPI およびその他のサービスプロバイダーを使用する場合の一般的なガイドラインに従ってください。 詳細については、「 [mapi アプリケーション開発](mapi-application-development.md)および[mapi サービスプロバイダ](mapi-service-providers.md)」を参照してください。
    
- トランスポートプロバイダ DLL が MAPI に公開される[](xpproviderinit.md)ようにします。 
    
- [ixpprovider: iunknown](ixpprovideriunknown.md)インターフェイスと[IXPLogon: iunknown](ixplogoniunknown.md)インターフェイスの実装を MAPI に公開します。 
    
- MAPI およびクライアントアプリケーションに対して、 [imapistatus: imapistatus](imapistatusimapiprop.md)インターフェイスの実装を公開します。 **imapistatus**の実装の詳細については、「 [status オブジェクトの実装](status-object-implementation.md)」を参照してください。 
    
- 構成用のプロパティシートダイアログボックスを実装します。 プロパティシートの実装の詳細については、「[プロパティシートの実装](property-sheet-implementation.md)」を参照してください。
    

