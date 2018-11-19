---
title: ADO/WFC プログラミング
TOCTitle: ADO/WFC programming
ms:assetid: fc438cc2-00b9-9590-6e0d-a865001ccf2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250293(v=office.15)
ms:contentKeyID: 48548887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 659e9dfe0e19b4ddb14513042f26fc80b11a00c3
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026065"
---
# <a name="adowfc-programming"></a>ADO/WFC プログラミング

**適用されます**Access 2013、Office 2013。

Microsoft Visual J++ 6.0 の場合、Windows Foundation Classes (WFC) と共に機能するように ADO が次のように拡張されました。まず、Java クラス セットの実装により ADO インターフェイスが拡張され、Java プログラマに役立つ通知が追加されました。また、Java クラスでは、Java 型をユーザーに返す関数も提供されます。パフォーマンスを向上させるため、Java クラスは、OLE DB 行セット オブジェクトのネイティブ データ型に直接アクセスし、バリアント型 (Variant) への変換やバリアント型からの変換を行わずに Java 型として Java プログラマに返します。また、ADO は、WFC フレームワークのイベント通知でも機能するように拡張されました。

Windows Foundation Classes 用の ADO (ADO/WFC) は、標準の ADO のメソッド、プロパティ、オブジェクト、およびイベントをすべてサポートしています。ただし、パラメーターとしてバリアント型 (variant) を必要とし、Microsoft Visual Basic などの言語で高いパフォーマンスを示すような操作を、Visual J++ などの言語で実行するとパフォーマンスが低下します。そのため、ADO/WFC では、[Field](field-object-ado.md) オブジェクトで、バリアント型のデータではなくネイティブな Java データ型を使用するアクセス機能を用意しています。

ADO/WFC パッケージの詳細については、ADO のマニュアルの「[ADO/WFC 構文インデックス](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/ado-wfc-syntax-index)」を参照してください。

## <a name="referencing-the-library"></a>ライブラリを参照します。

ADO/WFC データ クラスをプロジェクトにインポートするには、次の行をコードに追加します。

```java 
 
import com.ms.wfc.data.*; 
```

