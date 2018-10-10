---
title: IIS でプロセッサごとにスレッドを指定する
TOCTitle: Specifying Threads Per Processor on IIS
ms:assetid: 12889d7b-5415-8077-2ca0-1c3a96fb89ec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248898(v=office.15)
ms:contentKeyID: 48543344
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de3c8c99c7f615928ea0a0f1e15171cc90b25f3d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476794"
---
# <a name="specifying-threads-per-processor-on-iis"></a>IIS でプロセッサごとにスレッドを指定する


**適用されます**Access 2013 |。Office 2013

Internet Information Services 4.0 以降で RDS を使用する場合は、Web サーバーのレジストリを操作することによって、プロセッサごとに作成されるスレッドの数を制御できます。プロセッサごとのスレッド数は、トラフィックが多い場合や、トラフィックが少なくてもクエリのサイズが大きい場合に、パフォーマンスに影響することがあります。さまざまな状況を試したうえで、最適な設定値を見つける必要があります。

この設定の既定値を決定または変更する方法は、IIS 4.0 サーバーの構成によって異なります。

MDAC 2.1.2.4202.3 (GA) 以降が IIS サーバーにインストールされている場合、RDS では、ASP スクリプトで使用するのと同じコンポーネント サービス (Windows NT では Microsoft Transaction Services) を使用します。プロセッサごとのスレッド数の既定値は 10 です。この既定値を変更するには、サーバー レジストリに次のキーを追加する必要があります。

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

*MaxPoolThreads*は、21、\_の DWORD です。 それは具体的には追加しない限り、 *MaxPoolThreads*は、レジストリには表示されません。 有効な値の範囲は、5 から推奨最大値の 20 までです。 レジストリ キーに指定した値が*PoolThreadLimit*キー (同じパスの下にある) の値よりも大きい場合、 *PoolThreadLimit*の値が使用されます。

一方、MDAC 2.1 2.1.1.3711.11 (GA) 以前のバージョンが IIS サーバーにインストールされている場合は、プロセッサごとのスレッド数の既定値は 6 です。既定値を変更するには、IIS サーバーのレジストリに次のキーを追加する必要があります。

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

*ADCThreads*は、21、\_の DWORD です。 それは具体的には追加しない限り、 *ADCThreads*は、レジストリには表示されません。 有効な値の範囲は、1 から 50 までです。 レジストリ キーで指定した値が 50 より大きい場合は、最大値 (50) が使用されます。

