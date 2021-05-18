---
title: オブジェクトの無効化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bf7ef15ccfd9cd015771785bda9d6ad79415736b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407677"
---
# <a name="invalidating-an-object"></a>オブジェクトの無効化

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロバイダーのシャットダウン プロセスの一環として、オブジェクトを無効にしたい場合があります。 オブジェクトを無効にするには、その vtable を 3 つの **IUnknown** メソッド (AddRef、Release、QueryInterface) の実装を含む vtable に置き換 **える必要があります**。   [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)、3 つの一般的なプロバイダーの種類のそれぞれのサポート オブジェクトに含まれているメソッドを呼び出すことによって、オブジェクトを無効にします。 プロバイダーは通常、ログオン オブジェクトの Logoff メソッドの実装でこの呼 **び出しを行** います。 
  
オブジェクトを無効にすることで、MAPI はオブジェクトに関連付けられたメモリを解放する最終的な責任を負います。 オブジェクトに接続されているリソースをすべて解放し **、MakeInvalid** を呼び出して、継承されたインターフェイス内のすべてのメソッドを無効にできます。 これらのメソッドの呼び出しは、MAPI_E_INVALID_OBJECT。 **MakeInvalid の使用** は、多くのサービス プロバイダーが無視することを選択するオプションです。 
  
## <a name="see-also"></a>関連項目



[サービス プロバイダーのシャットダウン](shutting-down-a-service-provider.md)

