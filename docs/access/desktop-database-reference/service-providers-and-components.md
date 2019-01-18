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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717245"
---
# <a name="service-providers-and-components"></a>サービス プロバイダーとコンポーネント


**適用されます**Access 2013、Office 2013。

サービス プロバイダーは、データ ストアではネイティブにサポートされていない拡張インターフェイスを実装することにより、データ プロバイダーの機能を拡張するコンポーネントです。

Microsoft Data Access は、低機能のストア上にデータベースの機能、または、「サービス」セットを実装するために専門的な個別のコンポーネントを個別にできるようにするための*コンポーネント アーキテクチャ*を提供します。 したがって、独自の拡張機能の実装を提供するには、各データ ストアやデータベース機能を内部的に実装するために汎用的なアプリケーションを強制することではなくサービス コンポーネントは、一般的な実装であり、任意のアプリケーションことができます。任意のデータ ストアにアクセスするときに使用します。 データ ストアと、汎用コンポーネントを介して、いくつかの機能がネイティブに実装されているという事実は、アプリケーションに対して透過的です。

たとえば、Microsoft Cursor Service for OLE DB のようなカーソル エンジンは、前方のみの順次データ ストアのデータを使用して、スクロール可能なデータを生成するサービス コンポーネントです。通常 ADO で使用されるその他のサービス プロバイダーには、Microsoft OLE DB Persistence Provider (ファイルへのデータの保存用)、Microsoft Data Shaping Service for OLE DB (階層 **Recordsets** 用)、および Microsoft OLE DB Remoting Provider (リモート コンピューターでのデータ プロバイダーの呼び出し用) があります。

サービス プロバイダーとデータ プロバイダーの詳細については、「[付録 A: プロバイダー](appendix-a-providers.md)」を参照してください。

