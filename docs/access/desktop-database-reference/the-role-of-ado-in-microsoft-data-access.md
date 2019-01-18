---
title: Microsoft Data Access における ADO の役割
TOCTitle: The Role of ADO in Microsoft Data Access
ms:assetid: e9087ec8-850b-ebbe-369a-a5987a528de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250180(v=office.15)
ms:contentKeyID: 48548433
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 91f591513e0a35a70d157b0a640c87efc961fe22
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703175"
---
# <a name="role-of-ado-in-microsoft-data-access"></a>Microsoft Data Access における ADO の役割

**適用されます**Access 2013、Office 2013。

Microsoft Data Access Components (MDAC) は、データ ストア、ツール、および言語から独立したデータ アクセスを提供します。MDAC は、高レベルで使いやすいインターフェイス、および低レベルで高パフォーマンスのインターフェイスを、実質的に使用できるすべてのデータ ストアに提供します。この柔軟性を利用して、さまざまなデータ ストアを統合し、任意のツール、アプリケーション、およびプラットフォーム サービスを使用して、ニーズに合わせた的確なソリューションを作成できます。これらのテクノロジにより、Microsoft Windows オペレーティング システムにおける汎用的なデータ アクセスの基本的なフレームワークが提供されます。

MDAC には 3 つの主要なテクノロジがあります。ActiveX Data Objects (ADO) は、OLE DB への高レベルで使いやすいインターフェイスです。OLE DB は、さまざまなデータ ストアへの低レベルで高パフォーマンスのインターフェイスです。ADO と OLE DB は、リレーショナル (表形式) データと非リレーショナル (階層またはストリーム) データを処理できます。最後に、Open Database Connectivity (ODBC) は、リレーショナル データ ストア専用に設計された低レベルで高パフォーマンスのもう 1 つのインターフェイスです。

ADO には、クライアント アプリケーションまたは中間層アプリケーションと低レベルの OLE DB インターフェイスとの間に抽象層が用意されています。ADO は、小規模な Automation オブジェクト一式を使用して、OLE DB への単純で効率的なインターフェイスを提供します。このインターフェイスを使用することで、Visual Basic や VBScript などの高レベル言語を使用して、COM や OLE DB の複雑性を理解することなくデータにアクセスしようとする開発者にとって、ADO は最適な選択になります。

