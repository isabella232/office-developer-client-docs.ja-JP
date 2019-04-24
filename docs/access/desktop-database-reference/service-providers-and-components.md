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
# <a name="service-providers-and-components"></a><span data-ttu-id="6478e-102">サービス プロバイダーとコンポーネント</span><span class="sxs-lookup"><span data-stu-id="6478e-102">Service providers and components</span></span>


<span data-ttu-id="6478e-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="6478e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6478e-104">サービス プロバイダーは、データ ストアではネイティブにサポートされていない拡張インターフェイスを実装することにより、データ プロバイダーの機能を拡張するコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="6478e-104">Service providers are components that extend the functionality of data providers by implementing extended interfaces that are not natively supported by the data store.</span></span>

<span data-ttu-id="6478e-p101">Microsoft Data Access は、"コンポーネント アーキテクチャ" を提供することにより、データベース機能の個々の集合である "サービス" を、個別の専門化したコンポーネントが低機能のストアに対して実装できるようにします。つまりサービス コンポーネントにより、各データ ストアが拡張機能を独自に実装したり、汎用アプリケーションがデータベース機能を内部的に実装したりする必要がなくなり、データ ストアへのアクセス時にすべてのアプリケーションが使用できる共通の実装が提供されます。データ ストアによってネイティブで実装される機能と、汎用コンポーネントを介して実装される機能があることを、アプリケーションが意識することはありません。</span><span class="sxs-lookup"><span data-stu-id="6478e-p101">Microsoft Data Access provides a *component architecture* that allows individual, specialized components to implement discrete sets of database functionality, or "services," on top of less capable stores. Thus, rather than forcing each data store to provide its own implementation of extended functionality or forcing generic applications to implement database functionality internally, service components provide a common implementation that any application can use when accessing any data store. The fact that some functionality is implemented natively by the data store and some through generic components is transparent to the application.</span></span>

<span data-ttu-id="6478e-p102">たとえば、Microsoft Cursor Service for OLE DB のようなカーソル エンジンは、前方のみの順次データ ストアのデータを使用して、スクロール可能なデータを生成するサービス コンポーネントです。通常 ADO で使用されるその他のサービス プロバイダーには、Microsoft OLE DB Persistence Provider (ファイルへのデータの保存用)、Microsoft Data Shaping Service for OLE DB (階層 **Recordsets** 用)、および Microsoft OLE DB Remoting Provider (リモート コンピューターでのデータ プロバイダーの呼び出し用) があります。</span><span class="sxs-lookup"><span data-stu-id="6478e-p102">For example, a cursor engine, such as the Microsoft Cursor Service for OLE DB, is a service component that can consume data from a sequential, forward-only data store to produce scrollable data. Other service providers commonly used by ADO include the Microsoft OLE DB Persistence Provider (for saving data to a file), the Microsoft Data Shaping Service for OLE DB (for hierarchical **Recordsets**), and the Microsoft OLE DB Remoting Provider (for invoking data providers on a remote computer).</span></span>

<span data-ttu-id="6478e-110">サービス プロバイダーとデータ プロバイダーの詳細については、「[付録 A: プロバイダー](appendix-a-providers.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6478e-110">For more information about service and data providers, see [Appendix A: Providers](appendix-a-providers.md).</span></span>

