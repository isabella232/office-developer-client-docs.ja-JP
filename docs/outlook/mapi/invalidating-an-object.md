---
title: オブジェクトを無効にする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bf7ef15ccfd9cd015771785bda9d6ad79415736b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317200"
---
# <a name="invalidating-an-object"></a>オブジェクトを無効にする

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロバイダーのシャットダウンプロセスの一環として、オブジェクトを無効にすることもできます。 オブジェクトを無効にするには、3つの**IUnknown**メソッド ( **AddRef**、 **Release**、および**QueryInterface**) の実装を含む vtable に vtable を置き換える必要があります。 3つの一般的なプロバイダーの各種類の support オブジェクトに含まれているメソッドである[imapisupport:: makeinvalid](imapisupport-makeinvalid.md)を呼び出して、オブジェクトを無効にします。 プロバイダーは通常、この呼び出しをログオンオブジェクトの**Logoff**メソッドの実装で行います。 
  
オブジェクトを無効にすると、オブジェクトに関連付けられているメモリを解放するための最終的な責任が MAPI に提供されます。 オブジェクトに接続されているすべてのリソースを解放し、 **makeinvalid**を呼び出して、継承されたインターフェイス内のすべてのメソッドを無効にすることができます。 これらのメソッドを呼び出すと、MAPI_E_INVALID_OBJECT が返されます。 **makeinvalid**を使用することは、多くのサービスプロバイダーが無視することを選択するオプションです。 
  
## <a name="see-also"></a>関連項目



[サービスプロバイダーのシャットダウン](shutting-down-a-service-provider.md)

