---
title: ADO Java クラス ラッパー
TOCTitle: ADO Java Class Wrappers
ms:assetid: de50faf0-80f3-f295-3d9e-3f70f86c3ede
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250126(v=office.15)
ms:contentKeyID: 48548183
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 602d3407d78843331fdb78ef728cebbc69bace14
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889463"
---
# <a name="ado-java-class-wrappers"></a><span data-ttu-id="2a9e1-102">ADO Java クラス ラッパー</span><span class="sxs-lookup"><span data-stu-id="2a9e1-102">ADO Java Class Wrappers</span></span>


<span data-ttu-id="2a9e1-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="2a9e1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2a9e1-p101">このコードは、ADO [Recordset](recordset-object-ado.md) クラス ラッパーのインスタンスを宣言し、すべて同じコード行で初期化します。また、 [LockType](open-method-ado-recordset.md) と [CursorType](locktype-property-ado.md) などの [Open](cursortype-property-ado.md) メソッドの各引数の変数を宣言します (Java が列挙型をサポートしないため)。 **Recordset** オブジェクトを開いて閉じます。Rs1 を NULL に設定する操作は、単に Java のシステムが定期的に未使用のオブジェクトを解放するときに、この変数が解放されるようにスケジュールに入れることを意味します。</span><span class="sxs-lookup"><span data-stu-id="2a9e1-p101">This code declares an instance of the ADO [Recordset](recordset-object-ado.md) class wrapper and initializes it, all on the same line of code. Further, it declares variables for each of the arguments in the [Open](open-method-ado-recordset.md) method, especially for [LockType](locktype-property-ado.md) and [CursorType](cursortype-property-ado.md) (because Java doesn't support enumerated types). It opens and closes the **Recordset** object. Setting Rs1 to NULL merely schedules that variable to be released when Java performs its systematic and intermittent release of unused objects.</span></span>

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

