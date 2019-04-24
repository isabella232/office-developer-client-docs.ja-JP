---
title: MAPI のオブジェクトとインターフェイスの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d4ece3af-cb54-4727-8072-0c055381ec11
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fcd85bf518f4e6466bf15a09e417767bc34df78d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345788"
---
# <a name="mapi-object-and-interface-overview"></a>MAPI のオブジェクトとインターフェイスの概要

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
mapi オブジェクトは、1つ以上の mapi インターフェイスまたは関連する関数のコレクションから継承された C++ オブジェクトクラスまたは c データ構造です。 これらの関連する関数のコレクションは、C++ 開発者が純粋仮想関数として知られています。 純粋仮想関数の場合、MAPI は関数プロトタイプのみを提供し、実装は提供しません。 クライアントアプリケーション、サービスプロバイダー、または MAPI がこの実装を提供することは、インターフェイスを継承するオブジェクトクラスを作成し、メッセージング API の関数の説明に準拠していることを前提としています。 MAPI インターフェイスは、継承されたクラスによってのみインスタンス化できます。
  
さまざまな MAPI オブジェクトがあります。各オブジェクトは、最終的に[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)インターフェイスから継承されるインターフェイスから継承します。 **IUnknown**は、OLE コンポーネントオブジェクトモデル (COM) 基本インターフェイスです。 これは、通信と制御のための標準的なメカニズムを使用して MAPI オブジェクトを提供します。 COM は、オブジェクトの実装者がメモリ管理、パラメーター管理、マルチスレッドなどの問題をどのように処理するかを決定します。 このモデルに準拠することにより、オブジェクトの実装者は、オブジェクトに含まれているインターフェイスで指定されたコントラクトに準拠します。 
  
多くの MAPI インターフェイスは**IUnknown**から直接継承されていますが、他のインターフェイスは、 [imapiprop: iunknown](imapipropiunknown.md) for property management and [IMAPIContainer: imapiprop](imapicontainerimapiprop.md) for folder およびという2つの基本インターフェイスのいずれかによって間接的に継承されます。アドレス帳へのアクセス。 基本インターフェイスは、独立したスタンドアロンオブジェクトとしては実装されません。これらは常に、派生インターフェイスを実装するオブジェクトである他のオブジェクトの一部として実装されます。 
  
mapi は、それぞれが1つ以上の mapi コンポーネントによって実装された、さまざまな種類のオブジェクトを定義します。 クライアントによって実装されたオブジェクトは、MAPI、サービスプロバイダー、およびカスタムフォームコンポーネントによって使用されます。 サービスプロバイダーによって実装されるオブジェクトは、通常、MAPI およびクライアントによって使用されます。 フォームライブラリプロバイダおよびフォームサーバーによって実装されたオブジェクトは、他のフォームコンポーネントおよびクライアントによって使用されます。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MAPI の概念](mapi-concepts.md)

