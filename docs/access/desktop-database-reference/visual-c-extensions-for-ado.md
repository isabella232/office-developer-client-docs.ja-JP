---
title: ADO 用の Visual C++ Extensions
TOCTitle: Visual C++ Extensions for ADO
ms:assetid: 38048ae0-1dae-9e5e-c569-04011df8b5aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249134(v=office.15)
ms:contentKeyID: 48544212
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ddec21377543be5d76009bc37d7ceb7b8de38f2a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614921"
---
# <a name="visual-c-extensions-for-ado"></a>ADO 用 Visual C++ Extensions


**適用先**: Access 2013、Office 2013

ADO を使用してプログラミングするVisual C++、ADO プログラミングの説明に従って **\# 、import** ディレクティブ [Microsoft Visual C++使用します](visual-c-ado-programming.md)。 しかし、ADO の以前のバージョンでは、Visual C++ を使用するプログラミングの代替方法として、Visual C++ Extensions が提供されていました。 このセクションでは、拡張機能のコードを管理する必要Visual C++、インポートを使用して新しい ADO コードを記述する必要がある場合に、この機能について説明 \# **します**。

Visual C++ を使用するプログラマが、ADO でデータを取得する際に直面する手間のかかる作業の 1 つに、バリアント データ型 (Variant) として返されたデータを C++ データ型に変換し、変換したデータをさらにクラスまたは構造体に格納するという作業があります。バリアント データ型を使用して C++ データ型を取得すると、手間がかかるだけでなくパフォーマンスも低下します。

ADO には、バリアント型 (Variant) を使用しないでネイティブな C/C++ データ型のデータを取得できるインターフェイスと、そのインターフェイスを簡単に操作するためのプリプロセッサ マクロが用意されています。その結果、使用しやすく優れたパフォーマンスを持った、柔軟性のあるツールとなりました。

C/C++ クライアントでは、通常は、ネイティブ C/C++ 型を格納する C/C++ 構造体またはクラスに [Recordset](recordset-object-ado.md) のレコードをバインドします。バリアント型 (Variant) を使用する場合、バリアント型からネイティブ C/C++ 型に変換するコードを作成する必要があります。ADO 用の Visual C++ Extensions は、Visual C++ プログラマがこのような作業を簡単に行えるようにすることを目的としています。

ADO 用の Visual C++ Extensions の詳細については、次のトピックを参照してください。

  - [Visual C++ Extensions を使用する](using-visual-c-extensions.md)

  - [Visual C++ Extensions のヘッダー](visual-c-extensions-header.md)

  - [Visual C++ Extensions の例](visual-c-extensions-example.md)

