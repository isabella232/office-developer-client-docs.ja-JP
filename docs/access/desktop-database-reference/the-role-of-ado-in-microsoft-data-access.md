---
title: Microsoft Data Access における ADO の役割
TOCTitle: The Role of ADO in Microsoft Data Access
ms:assetid: e9087ec8-850b-ebbe-369a-a5987a528de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250180(v=office.15)
ms:contentKeyID: 48548433
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b0812e87c961110f6ee7afc8e0909c85b6197df3
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944950"
---
# <a name="role-of-ado-in-microsoft-data-access"></a><span data-ttu-id="9c58d-102">Microsoft Data Access における ADO の役割</span><span class="sxs-lookup"><span data-stu-id="9c58d-102">Role of ADO in Microsoft Data Access</span></span>

<span data-ttu-id="9c58d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="9c58d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9c58d-p101">Microsoft Data Access Components (MDAC) は、データ ストア、ツール、および言語から独立したデータ アクセスを提供します。MDAC は、高レベルで使いやすいインターフェイス、および低レベルで高パフォーマンスのインターフェイスを、実質的に使用できるすべてのデータ ストアに提供します。この柔軟性を利用して、さまざまなデータ ストアを統合し、任意のツール、アプリケーション、およびプラットフォーム サービスを使用して、ニーズに合わせた的確なソリューションを作成できます。これらのテクノロジにより、Microsoft Windows オペレーティング システムにおける汎用的なデータ アクセスの基本的なフレームワークが提供されます。</span><span class="sxs-lookup"><span data-stu-id="9c58d-p101">The Microsoft Data Access Components (MDAC) provide data access that is independent of data stores, tools, and languages. It provides a high-level, easy-to-use interface, and a low-level, high-performance interface to practically any data store available. You can use this flexibility to integrate diverse data stores and use your choice of tools, applications, and platform services to create the right solutions for your needs. These technologies provide the basic framework for general-purpose data access in Microsoft Windows operating systems.</span></span>

<span data-ttu-id="9c58d-p102">MDAC には 3 つの主要なテクノロジがあります。ActiveX Data Objects (ADO) は、OLE DB への高レベルで使いやすいインターフェイスです。OLE DB は、さまざまなデータ ストアへの低レベルで高パフォーマンスのインターフェイスです。ADO と OLE DB は、リレーショナル (表形式) データと非リレーショナル (階層またはストリーム) データを処理できます。最後に、Open Database Connectivity (ODBC) は、リレーショナル データ ストア専用に設計された低レベルで高パフォーマンスのもう 1 つのインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="9c58d-p102">There are three primary technologies in MDAC. ActiveX Data Objects (ADO) is a high-level, easy-to-use interface to OLE DB. OLE DB is a low-level, high-performance interface to a variety of data stores. ADO and OLE DB both can work with relational (tabular) and nonrelational (hierarchical or stream) data. Finally, Open Database Connectivity (ODBC) is another low-level, high-performance interface that is designed specifically for relational data stores.</span></span>

<span data-ttu-id="9c58d-p103">ADO には、クライアント アプリケーションまたは中間層アプリケーションと低レベルの OLE DB インターフェイスとの間に抽象層が用意されています。ADO は、小規模な Automation オブジェクト一式を使用して、OLE DB への単純で効率的なインターフェイスを提供します。このインターフェイスを使用することで、Visual Basic や VBScript などの高レベル言語を使用して、COM や OLE DB の複雑性を理解することなくデータにアクセスしようとする開発者にとって、ADO は最適な選択になります。</span><span class="sxs-lookup"><span data-stu-id="9c58d-p103">ADO provides a layer of abstraction between your client or middle-tier application and the low-level OLE DB interfaces. ADO uses a small set of Automation objects to provide a simple and efficient interface to OLE DB. This interface makes ADO the perfect choice for developers in higher level languages, such as Visual Basic and even VBScript, who want to access data without having to learn the intricacies of COM and OLE DB.</span></span>

