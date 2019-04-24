---
title: DCOM ストリーム マーシャリング形式の設定
TOCTitle: Setting DCOM stream marshaling format
ms:assetid: 5f75fc59-a9f8-6686-07f9-de292e4da787
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249346(v=office.15)
ms:contentKeyID: 48545162
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 09463552faff9c4b74b73379385ab8ba55b4f62c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308667"
---
# <a name="setting-dcom-stream-marshaling-format"></a>DCOM ストリーム マーシャリング形式の設定


**適用先:** Access 2013、Office 2013

RDS 1.5 以前のコンポーネントを使っているクライアント コンピューターは、RDS 2.0 以降のコンポーネントを使っているサーバーとは互換性がありません。基になるプロトコルとして DCOM を使っている場合は、RDS 2.0 以降をサポートする方が [Recordset](recordset-object-ado.md) オブジェクトの転送において効率的です。クライアントで RDS 1.5 以前のコンポーネントを実行している場合は、サーバーを古い RDS サポート (RDS 1.0) または新しい RDS サポート (RDS 2.0 以降) で動作するように設定できます。次のいずれかのレジストリ エントリを設定してください。

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS10" 
```

\-や

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS20" 
```

