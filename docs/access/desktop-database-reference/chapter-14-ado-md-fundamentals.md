---
title: '第 14 章: ADO MD の基本事項'
TOCTitle: 'Chapter 14: ADO MD fundamentals'
ms:assetid: 129baa54-0bc1-985d-4bfd-25a1c1c3018e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248899(v=office.15)
ms:contentKeyID: 48543346
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1a3b816c44b6b3b5e50a8ed492e1ca6240c920b4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627101"
---
# <a name="chapter-14-ado-md-fundamentals"></a>第 14 章: ADO MD の基本事項

**適用先**: Access 2013、Office 2013

Microsoft ActiveX データ オブジェクト (多次元) (ADO MD) を使用すると、Microsoft Visual Basic、Microsoft Visual C++、Microsoft Visual J++ などの言語から多次元データに簡単にアクセスできます。ADO MD は Microsoft ActiveX データ オブジェクト (ADO) を拡張したもので、[CubeDef](cubedef-object-ado-md.md) オブジェクトや [Cellset](cellset-object-ado-md.md) オブジェクトのような多次元データ固有のオブジェクトが含まれています。ADO MD を使用すると、多次元スキーマを参照し、キューブにクエリを行い、その結果を取得できます。

ADO と同様、ADO MD でも、基になる OLE DB プロバイダーを使用してデータにアクセスします。ADO MD を使用して作業するためには、プロバイダーが OLE DB for OLAP の仕様で定義された多次元データ プロバイダー (MDP) である必要があります。MDP は、データを表形式のビューで表示する表形式データ プロバイダー (TDP) とは異なり、データを多次元のビューで表示します。使用する OLAP OLE DB プロバイダーでサポートされている具体的な構文や動作の詳細については、そのプロバイダーのドキュメントを参照してください。

このマニュアルは、Visual Basic プログラミング言語についての実践的な知識、および ADO と OLAP についての一般的な知識があることを前提としています。 詳細については [、「ADO](ado-programmer-s-guide.md) プログラマ ガイド」と「OLE DB for OLAP プログラマリファレンス」を参照してください。 

この章では、次のトピックについて説明します。

- [多次元スキーマとデータの概要](overview-of-multidimensional-schemas-and-data.md)
- [多次元データの使用](working-with-multidimensional-data.md)
- [ADO と ADO MD を共に使用する](using-ado-with-ado-md.md)
- [ADO MD を使ってプログラミングする](programming-with-ado-md.md)
