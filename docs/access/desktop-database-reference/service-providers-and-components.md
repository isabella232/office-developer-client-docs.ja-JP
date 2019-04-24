---
title: サービス プロバイダーとコンポーネント
TOCTitle: Service Providers and Components
ms:assetid: e42d9c84-525a-4aca-01b2-88e3f2b0717f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250163(v=office.15)
ms:contentKeyID: 48548333
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 03447b9977c74484eb7455a75fc2255c33c5e4c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308702"
---
# <a name="service-providers-and-components"></a>サービス プロバイダーとコンポーネント


**適用先:** Access 2013、Office 2013

サービス プロバイダーは、データ ストアではネイティブにサポートされていない拡張インターフェイスを実装することにより、データ プロバイダーの機能を拡張するコンポーネントです。

Microsoft Data Access は、"コンポーネント アーキテクチャ" を提供することにより、データベース機能の個々の集合である "サービス" を、個別の専門化したコンポーネントが低機能のストアに対して実装できるようにします。つまりサービス コンポーネントにより、各データ ストアが拡張機能を独自に実装したり、汎用アプリケーションがデータベース機能を内部的に実装したりする必要がなくなり、データ ストアへのアクセス時にすべてのアプリケーションが使用できる共通の実装が提供されます。データ ストアによってネイティブで実装される機能と、汎用コンポーネントを介して実装される機能があることを、アプリケーションが意識することはありません。

たとえば、Microsoft Cursor Service for OLE DB のようなカーソル エンジンは、前方のみの順次データ ストアのデータを使用して、スクロール可能なデータを生成するサービス コンポーネントです。通常 ADO で使用されるその他のサービス プロバイダーには、Microsoft OLE DB Persistence Provider (ファイルへのデータの保存用)、Microsoft Data Shaping Service for OLE DB (階層 **Recordsets** 用)、および Microsoft OLE DB Remoting Provider (リモート コンピューターでのデータ プロバイダーの呼び出し用) があります。

サービス プロバイダーとデータ プロバイダーの詳細については、「[付録 A: プロバイダー](appendix-a-providers.md)」を参照してください。

