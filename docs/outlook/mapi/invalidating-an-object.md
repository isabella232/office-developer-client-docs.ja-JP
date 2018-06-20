---
title: オブジェクトを無効化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 9c0ba8f1f0bf31bb892f380df310cd9fa7a8a24f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801093"
---
# <a name="invalidating-an-object"></a>オブジェクトを無効化

  
  
**適用されます**: Outlook 
  
プロバイダーのシャット ダウン プロセスの一環として、オブジェクトを無効にすることもできます。 オブジェクトが無効では、vtable と vtable が同じ 3 つの**IUnknown**メソッドの実装が含まれている: **AddRef**、**リリース**、および**バージョン管理規則によって**。 [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)、3 つの一般的なプロバイダーの種類のそれぞれのサポート オブジェクトに含まれるメソッドを呼び出すことによってオブジェクトを無効にします。 プロバイダーは、通常、ログオン オブジェクトの**ログオフ時**のメソッドの実装ではこの呼び出しを作成します。 
  
MAPI オブジェクトに関連付けられているメモリを解放する最終的な責任は、オブジェクトを無効にします。 すべてのオブジェクトに接続されているリソースを解放し、すべての継承されたインターフェイスのメソッドを無効にする**MakeInvalid**を呼び出してできます。 これらのメソッドへの呼び出しには、MAPI_E_INVALID_OBJECT が返されます。 **MakeInvalid**を使用して、無視するように多くのサービス プロバイダーを選択するオプションです。 
  
## <a name="see-also"></a>関連項目



[サービス プロバイダーをシャット ダウン](shutting-down-a-service-provider.md)

