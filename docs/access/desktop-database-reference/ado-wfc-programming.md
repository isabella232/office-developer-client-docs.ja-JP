---
title: ADO/WFC プログラミング
TOCTitle: ADO/WFC programming
ms:assetid: fc438cc2-00b9-9590-6e0d-a865001ccf2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250293(v=office.15)
ms:contentKeyID: 48548887
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 904b5e3930c0e7e7b1d98f94bd39cfbf816aa145
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283206"
---
# <a name="adowfc-programming"></a>ADO/WFC プログラミング

**適用先:** Access 2013、Office 2013

Microsoft Visual J++ 6.0 の場合、Windows Foundation Classes (WFC) と共に機能するように ADO が次のように拡張されました。まず、Java クラス セットの実装により ADO インターフェイスが拡張され、Java プログラマに役立つ通知が追加されました。また、Java クラスでは、Java 型をユーザーに返す関数も提供されます。パフォーマンスを向上させるため、Java クラスは、OLE DB 行セット オブジェクトのネイティブ データ型に直接アクセスし、バリアント型 (Variant) への変換やバリアント型からの変換を行わずに Java 型として Java プログラマに返します。また、ADO は、WFC フレームワークのイベント通知でも機能するように拡張されました。

Windows Foundation Classes 用の ADO (ADO/WFC) は、標準の ADO のメソッド、プロパティ、オブジェクト、およびイベントをすべてサポートしています。ただし、パラメーターとしてバリアント型 (variant) を必要とし、Microsoft Visual Basic などの言語で高いパフォーマンスを示すような操作を、Visual J++ などの言語で実行するとパフォーマンスが低下します。そのため、ADO/WFC では、[Field](field-object-ado.md) オブジェクトで、バリアント型のデータではなくネイティブな Java データ型を使用するアクセス機能を用意しています。

ADO/WFC パッケージの詳細については、ADO のマニュアルの「[ADO/WFC 構文インデックス](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/ado-wfc-syntax-index)」を参照してください。

## <a name="referencing-the-library"></a>ライブラリの参照

ADO/WFC データ クラスをプロジェクトにインポートするには、次の行をコードに追加します。

```java 
 
import com.ms.wfc.data.*; 
```

