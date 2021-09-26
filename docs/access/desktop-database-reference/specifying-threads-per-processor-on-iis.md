---
title: IIS でのプロセッサごとのスレッドの指定
TOCTitle: Specifying threads per processor on IIS
ms:assetid: 12889d7b-5415-8077-2ca0-1c3a96fb89ec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248898(v=office.15)
ms:contentKeyID: 48543344
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f933b7e8fedcfcac42a99a067ea10c4029ccf4d9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621795"
---
# <a name="specifying-threads-per-processor-on-iis"></a>IIS でのプロセッサごとのスレッドの指定


**適用先**: Access 2013、Office 2013

RDS を インターネット インフォメーション サービス 4.0 以降で使用する場合は、Web サーバー上のレジストリを操作することで、プロセッサごとに作成されるスレッドの数を制御できます。 プロセッサごとのスレッド数は、トラフィックが多い場合や、トラフィックが少なくてもクエリのサイズが大きい場合に、パフォーマンスに影響することがあります。 さまざまな状況を試したうえで、最適な設定値を見つける必要があります。

この設定の既定値を決定または変更する方法は、IIS 4.0 サーバーの構成によって異なります。

MDAC 2.1.2.4202.3 (GA) 以降が IIS サーバーにインストールされている場合、RDS では、ASP スクリプトで使用するのと同じコンポーネント サービス (Windows NT では Microsoft Transaction Services) を使用します。プロセッサごとのスレッド数の既定値は 10 です。この既定値を変更するには、サーバー レジストリに次のキーを追加する必要があります。

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

*MaxPoolThreads は* REG \_ DWORD です。 *MaxPoolThreads* は、指定して追加しない限り、レジストリには表示されません。 有効な値の範囲は、5 から推奨最大値の 20 までです。 レジストリ キーで指定した値が *PoolThreadLimit* キー (同じパスにあります) の値より大きい場合、*PoolThreadLimit* の値が使用されます。

一方、MDAC 2.1 2.1.1.3711.11 (GA) 以前のバージョンが IIS サーバーにインストールされている場合は、プロセッサごとのスレッド数の既定値は 6 です。既定値を変更するには、IIS サーバーのレジストリに次のキーを追加する必要があります。

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

*ADCThreads は* REG \_ DWORD です。 *ADCThreads* は、指定して追加しない限り、レジストリには表示されません。 有効な値の範囲は、1 から 50 までです。 レジストリ キーで指定した値が 50 より大きい場合は、最大値 (50) が使用されます。

