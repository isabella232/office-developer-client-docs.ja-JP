---
title: ADO 用の Visual C++ Extensions
TOCTitle: Visual C++ Extensions for ADO
ms:assetid: 38048ae0-1dae-9e5e-c569-04011df8b5aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249134(v=office.15)
ms:contentKeyID: 48544212
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fc69d3244cf6faf3aa91fe954e4b39323cf13abf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302755"
---
# <a name="visual-c-extensions-for-ado"></a>ADO 用 Visual C++ Extensions


**適用先:** Access 2013、Office 2013

visual c++ で ado をプログラミングする方法として推奨されるのは、「 [Microsoft visual c++ ado プログラミング](visual-c-ado-programming.md)」で説明されているように、 ** \#import**ディレクティブを使用する方法です。 しかし、ADO の以前のバージョンでは、Visual C++ を使用するプログラミングの代替方法として、Visual C++ Extensions が提供されていました。 このセクションでは、Visual C++ Extensions コードを維持する必要がある場合にこの機能について説明\#します。ただし、新しい ADO コードは**import**を使用して記述する必要があります。

Visual C++ を使用するプログラマが、ADO でデータを取得する際に直面する手間のかかる作業の 1 つに、バリアント データ型 (Variant) として返されたデータを C++ データ型に変換し、変換したデータをさらにクラスまたは構造体に格納するという作業があります。バリアント データ型を使用して C++ データ型を取得すると、手間がかかるだけでなくパフォーマンスも低下します。

ADO には、バリアント型 (Variant) を使用しないでネイティブな C/C++ データ型のデータを取得できるインターフェイスと、そのインターフェイスを簡単に操作するためのプリプロセッサ マクロが用意されています。その結果、使用しやすく優れたパフォーマンスを持った、柔軟性のあるツールとなりました。

C/C++ クライアントでは、通常は、ネイティブ C/C++ 型を格納する C/C++ 構造体またはクラスに [Recordset](recordset-object-ado.md) のレコードをバインドします。バリアント型 (Variant) を使用する場合、バリアント型からネイティブ C/C++ 型に変換するコードを作成する必要があります。ADO 用の Visual C++ Extensions は、Visual C++ プログラマがこのような作業を簡単に行えるようにすることを目的としています。

ADO 用の Visual C++ Extensions の詳細については、次のトピックを参照してください。

  - [Visual C++ Extensions を使用する](using-visual-c-extensions.md)

  - [Visual C++ Extensions のヘッダー](visual-c-extensions-header.md)

  - [Visual C++ Extensions の例](visual-c-extensions-example.md)

