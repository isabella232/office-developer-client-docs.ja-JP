---
title: DCOM ストリーム マーシャリング形式を設定する
TOCTitle: Setting DCOM Stream Marshaling Format
ms:assetid: 5f75fc59-a9f8-6686-07f9-de292e4da787
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249346(v=office.15)
ms:contentKeyID: 48545162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 51449286d2ddd9340f1adc883cdaff7e76429f88
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874112"
---
# <a name="setting-dcom-stream-marshaling-format"></a><span data-ttu-id="99ae3-102">DCOM ストリーム マーシャリング形式を設定する</span><span class="sxs-lookup"><span data-stu-id="99ae3-102">Setting DCOM Stream Marshaling Format</span></span>


<span data-ttu-id="99ae3-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="99ae3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="99ae3-p101">RDS 1.5 以前のコンポーネントを使っているクライアント コンピューターは、RDS 2.0 以降のコンポーネントを使っているサーバーとは互換性がありません。基になるプロトコルとして DCOM を使っている場合は、RDS 2.0 以降をサポートする方が [Recordset](recordset-object-ado.md) オブジェクトの転送において効率的です。クライアントで RDS 1.5 以前のコンポーネントを実行している場合は、サーバーを古い RDS サポート (RDS 1.0) または新しい RDS サポート (RDS 2.0 以降) で動作するように設定できます。次のいずれかのレジストリ エントリを設定してください。</span><span class="sxs-lookup"><span data-stu-id="99ae3-p101">A client computer using components from RDS 1.5 or earlier is not compatible with a server using components from RDS 2.0 or later. When using DCOM as the underlying protocol, the support for RDS 2.0 or later is more efficient in transporting [Recordset](recordset-object-ado.md) objects. If your client is running components from RDS 1.5 or earlier, you can set your server to work with the previous RDS support (called RDS 1.0) or the newer RDS support (called RDS 2.0 or later). Set either of the following registry entries:</span></span>

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS10" 
```

<span data-ttu-id="99ae3-108">\-または -</span><span class="sxs-lookup"><span data-stu-id="99ae3-108">\-or-</span></span>

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS20" 
```

