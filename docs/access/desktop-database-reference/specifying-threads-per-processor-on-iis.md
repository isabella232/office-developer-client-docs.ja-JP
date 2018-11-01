---
title: IIS でプロセッサごとにスレッドを指定する
TOCTitle: Specifying Threads Per Processor on IIS
ms:assetid: 12889d7b-5415-8077-2ca0-1c3a96fb89ec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248898(v=office.15)
ms:contentKeyID: 48543344
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4212b1c2bcf89badedbc7a3b7d4dc72a879a95c7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871984"
---
# <a name="specifying-threads-per-processor-on-iis"></a>IIS でプロセッサごとにスレッドを指定する


**適用されます**Access 2013、Office 2013。

RDS のインターネット情報サービス 4.0 以降を使用している場合は、web サーバー上のレジストリを操作することでプロセッサごとに作成されるスレッドの数を制御できます。 プロセッサごとのスレッド数は、トラフィックが多い場合や、トラフィックが少なくてもクエリのサイズが大きい場合に、パフォーマンスに影響することがあります。 さまざまな状況を試したうえで、最適な設定値を見つける必要があります。

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

