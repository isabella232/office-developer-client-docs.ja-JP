---
title: サービス プロバイダーおよびコンポーネント
TOCTitle: Service Providers and Components
ms:assetid: e42d9c84-525a-4aca-01b2-88e3f2b0717f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250163(v=office.15)
ms:contentKeyID: 48548333
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bd75314cc3f1fbdb110b6c5647894887e400ca1e
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947631"
---
# <a name="service-providers-and-components"></a><span data-ttu-id="68e66-102">サービス プロバイダーおよびコンポーネント</span><span class="sxs-lookup"><span data-stu-id="68e66-102">Service providers and components</span></span>


<span data-ttu-id="68e66-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="68e66-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="68e66-104">サービス プロバイダーは、データ ストアではネイティブにサポートされていない拡張インターフェイスを実装することにより、データ プロバイダーの機能を拡張するコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="68e66-104">Service providers are components that extend the functionality of data providers by implementing extended interfaces that are not natively supported by the data store.</span></span>

<span data-ttu-id="68e66-105">Microsoft Data Access は、低機能のストア上にデータベースの機能、または、「サービス」セットを実装するために専門的な個別のコンポーネントを個別にできるようにするための*コンポーネント アーキテクチャ*を提供します。</span><span class="sxs-lookup"><span data-stu-id="68e66-105">Microsoft Data Access provides a *component architecture* that allows individual, specialized components to implement discrete sets of database functionality, or "services," on top of less capable stores.</span></span> <span data-ttu-id="68e66-106">したがって、独自の拡張機能の実装を提供するには、各データ ストアやデータベース機能を内部的に実装するために汎用的なアプリケーションを強制することではなくサービス コンポーネントは、一般的な実装であり、任意のアプリケーションことができます。任意のデータ ストアにアクセスするときに使用します。</span><span class="sxs-lookup"><span data-stu-id="68e66-106">Thus, rather than forcing each data store to provide its own implementation of extended functionality or forcing generic applications to implement database functionality internally, service components provide a common implementation that any application can use when accessing any data store.</span></span> <span data-ttu-id="68e66-107">データ ストアと、汎用コンポーネントを介して、いくつかの機能がネイティブに実装されているという事実は、アプリケーションに対して透過的です。</span><span class="sxs-lookup"><span data-stu-id="68e66-107">The fact that some functionality is implemented natively by the data store and some through generic components is transparent to the application.</span></span>

<span data-ttu-id="68e66-p102">たとえば、Microsoft Cursor Service for OLE DB のようなカーソル エンジンは、前方のみの順次データ ストアのデータを使用して、スクロール可能なデータを生成するサービス コンポーネントです。通常 ADO で使用されるその他のサービス プロバイダーには、Microsoft OLE DB Persistence Provider (ファイルへのデータの保存用)、Microsoft Data Shaping Service for OLE DB (階層 **Recordsets** 用)、および Microsoft OLE DB Remoting Provider (リモート コンピューターでのデータ プロバイダーの呼び出し用) があります。</span><span class="sxs-lookup"><span data-stu-id="68e66-p102">For example, a cursor engine, such as the Microsoft Cursor Service for OLE DB, is a service component that can consume data from a sequential, forward-only data store to produce scrollable data. Other service providers commonly used by ADO include the Microsoft OLE DB Persistence Provider (for saving data to a file), the Microsoft Data Shaping Service for OLE DB (for hierarchical **Recordsets**), and the Microsoft OLE DB Remoting Provider (for invoking data providers on a remote computer).</span></span>

<span data-ttu-id="68e66-110">サービス プロバイダーとデータ プロバイダーの詳細については、「[付録 A: プロバイダー](appendix-a-providers.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="68e66-110">For more information about service and data providers, see [Appendix A: Providers](appendix-a-providers.md).</span></span>

