---
title: '第 14 章: ADO MD の基本事項'
TOCTitle: 'Chapter 14: ADO MD Fundamentals'
ms:assetid: 129baa54-0bc1-985d-4bfd-25a1c1c3018e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248899(v=office.15)
ms:contentKeyID: 48543346
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e9e89673dcb5cce124747d914f63d1a38353aebe
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885746"
---
# <a name="chapter-14-ado-md-fundamentals"></a>第 14 章: ADO MD の基本事項


**適用されます**Access 2013、Office 2013。

Microsoft ActiveX データ オブジェクト (多次元) (ADO MD) を使用すると、Microsoft Visual Basic、Microsoft Visual C++、Microsoft Visual J++ などの言語から多次元データに簡単にアクセスできます。ADO MD は Microsoft ActiveX データ オブジェクト (ADO) を拡張したもので、[CubeDef](cubedef-object-ado-md.md) オブジェクトや [Cellset](cellset-object-ado-md.md) オブジェクトのような多次元データ固有のオブジェクトが含まれています。ADO MD を使用すると、多次元スキーマを参照し、キューブにクエリを行い、その結果を取得できます。

ADO MD は、ADO と同様に、基になる OLE DB プロバイダーを使用してデータにアクセスします。ADO MD を使用するには、プロバイダーが、OLE DB for OLAP 仕様で定義された多次元データ プロバイダー (MDP) である必要があります。MDP は、データを表形式で表示する表形式データ プロバイダー (TDP) とは対照的に、多次元表示のデータを表します。プロバイダーがサポートしている特定の構文と動作の詳細については、使用する OLAP OLE DB プロバイダーのマニュアルを参照してください。

このマニュアルは、Visual Basic プログラミング言語についての実践的な知識、および ADO と OLAP についての一般的な知識があることを前提としています。 詳細については、「[ADO プログラマ ガイド](ado-programmer-s-guide.md)」および「OLE DB Programmer's Reference」 (英語) の OLE DB for OLAP に関する記述を参照してください。 

この章では、次のトピックについて説明します。

- [多次元スキーマおよびデータの概要](overview-of-multidimensional-schemas-and-data.md)

- [多次元データを処理する](working-with-multidimensional-data.md)

- [ADO と ADO MD を共に使用する](using-ado-with-ado-md.md)

- [ADO MD を使ってプログラミングする](programming-with-ado-md.md)
