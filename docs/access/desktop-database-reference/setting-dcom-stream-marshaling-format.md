---
title: DCOM ストリーム マーシャリング形式を設定する
TOCTitle: Setting DCOM Stream Marshaling Format
ms:assetid: 5f75fc59-a9f8-6686-07f9-de292e4da787
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249346(v=office.15)
ms:contentKeyID: 48545162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c0c05a378624f118f1bf6f070273b686a2e50a6e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477999"
---
# <a name="setting-dcom-stream-marshaling-format"></a>DCOM ストリーム マーシャリング形式を設定する


**適用されます**Access 2013 |。Office 2013

RDS 1.5 以前のコンポーネントを使っているクライアント コンピューターは、RDS 2.0 以降のコンポーネントを使っているサーバーとは互換性がありません。基になるプロトコルとして DCOM を使っている場合は、RDS 2.0 以降をサポートする方が [Recordset](recordset-object-ado.md) オブジェクトの転送において効率的です。クライアントで RDS 1.5 以前のコンポーネントを実行している場合は、サーバーを古い RDS サポート (RDS 1.0) または新しい RDS サポート (RDS 2.0 以降) で動作するように設定できます。次のいずれかのレジストリ エントリを設定してください。

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS10" 
```

\-または -

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS20" 
```

