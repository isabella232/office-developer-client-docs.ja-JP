---
title: MAPI オブジェクトとインターフェイスの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d4ece3af-cb54-4727-8072-0c055381ec11
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d60f1bc4863986adf3d539c35f924a39e18beda9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595806"
---
# <a name="mapi-object-and-interface-overview"></a>MAPI オブジェクトとインターフェイスの概要

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI オブジェクトは、1 つ以上の MAPI インターフェイスまたは関連する関数のコレクションから継承された C++ オブジェクト クラスまたは C データ構造です。 関連する関数のこれらのコレクションは、純粋な仮想関数として C++ 開発者に知られています。 純粋な仮想関数の場合、MAPI は実装ではなく関数プロトタイプのみを提供します。 クライアント アプリケーション、サービス プロバイダー、または MAPI が、インターフェイスから継承し、Messaging API の関数の説明に準拠するオブジェクト クラスを作成することで、この実装を提供する必要があります。 MAPI インターフェイスは、継承されたクラスを通じてのみインスタンス化できます。
  
[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)インターフェイスから最終的に継承されるインターフェイスから継承する各オブジェクトには、さまざまな MAPI オブジェクトがあります。 **IUnknown は** OLE コンポーネント オブジェクト モデル (COM) ベース インターフェイスです。 MAPI オブジェクトには、通信と制御のための標準的なメカニズムが提供されます。 COM は、オブジェクト実装者がメモリ管理、パラメーター管理、マルチスレッドなどの問題を処理する方法を指定します。 このモデルに準拠することで、オブジェクト実装者は、オブジェクトに含まれるインターフェイスで指定されたコントラクトに従います。 
  
多くの MAPI インターフェイスは **IUnknown** から直接継承されます。他のインターフェイスは [、IMAPIProp : IUnknown](imapipropiunknown.md) for property management および [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) for folder and address book access の 2 つのベース インターフェイスのいずれかを介して間接的に継承されます。 基本インターフェイスは、独立したスタンドアロン オブジェクトとして実装されません。これらは、派生インターフェイスを実装する他のオブジェクト、オブジェクトの一部として常に実装されます。 
  
MAPI では、1 つ以上の MAPI コンポーネントによって実装されるさまざまな種類のオブジェクトを定義します。 クライアントによって実装されたオブジェクトは、MAPI、サービス プロバイダー、およびカスタム フォーム コンポーネントによって使用されます。 サービス プロバイダーによって実装されるオブジェクトは、通常、MAPI およびクライアントによって使用されます。 フォーム ライブラリ プロバイダーとフォーム サーバーによって実装されたオブジェクトは、他のフォーム コンポーネントやクライアントによって使用されます。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MAPI の概念](mapi-concepts.md)

