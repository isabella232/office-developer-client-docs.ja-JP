---
title: ADO Java ラッパー
TOCTitle: ADO Java class wrappers
ms:assetid: de50faf0-80f3-f295-3d9e-3f70f86c3ede
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250126(v=office.15)
ms:contentKeyID: 48548183
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ccbd0b330de051b29d0ed3739c35720423ffc995
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553348"
---
# <a name="ado-java-class-wrappers"></a>ADO Java ラッパー


**適用先:** Access 2013、Office 2013

このコードは、ADO [Recordset](recordset-object-ado.md) クラス ラッパーのインスタンスを宣言し、すべて同じコード行で初期化します。また、 [LockType](open-method-ado-recordset.md) と [CursorType](locktype-property-ado.md) などの [Open](cursortype-property-ado.md) メソッドの各引数の変数を宣言します (Java が列挙型をサポートしないため)。 **Recordset** オブジェクトを開いて閉じます。Rs1 を NULL に設定する操作は、単に Java のシステムが定期的に未使用のオブジェクトを解放するときに、この変数が解放されるようにスケジュールに入れることを意味します。

```java 
 
public static void main( String args[]) 
{ 
 msado15._Recordset Rs1 = new msado15.Recordset(); 
 Variant Source = new Variant( "SELECT * FROM Authors" ); 
 Variant Connect = new Variant( "DSN=AdoDemo;UID=admin;PWD=;" ); 
 int LockType = msado15.CursorTypeEnum.adOpenForwardOnly; 
 int CursorType = msado15.LockTypeEnum.adLockReadOnly; 
 int Options = -1; 
 
 Rs1.Open( Source, Connect, LockType, CursorType, Options ); 
 Rs1.Close(); 
 Rs1 = null; 
 
 System.out.println( "Success!\n" ); 
} 
```

