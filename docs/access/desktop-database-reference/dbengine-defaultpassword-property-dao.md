---
title: DBEngine.DefaultPassword プロパティ (DAO)
TOCTitle: DefaultPassword Property
ms:assetid: 189e34f3-d573-c75f-8be2-d98c50df8a52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845616(v=office.15)
ms:contentKeyID: 48543478
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 50aa757b7f481aca22c087914f99660020439975
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615600"
---
# <a name="dbenginedefaultpassword-property-dao"></a>DBEngine.DefaultPassword プロパティ (DAO)


**適用先**: Access 2013、Office 2013

既定の **Workspace** を作成するために初期化時に使用されるパスワードを設定します。値の取得および設定が可能です。文字列型 ( **String**) の値を使用します。

## <a name="syntax"></a>構文

*式* .DefaultPassword

*式* **DBEngine** オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**DefaultPassword** の設定値は、最大 20 文字の文字列データ型 (String) です。このプロパティには、ASCII の 0 を除くすべての文字を含めることができます。


> [!NOTE]
> [!メモ] パスワードには、大文字、小文字、数字、記号を組み合わせた複雑なものを使用してください。これらの文字を混在させたものになっていないパスワードは強固とはいえません。たとえば、Y6dh!et5 は安全性の高いパスワードです。House27 は推測されやすいパスワードです。また、高い安全性を保ちながらも、書き留めておかなくても覚えておくことができるパスワードを使用してください。

既定では、 **DefaultUser** プロパティは "admin" に設定され、 **DefaultPassword** プロパティは長さが 0 の文字列 ("") に設定されます。

Typically, you use the **CreateWorkspace** method to create a **Workspace** object with a given user name and password. However, for backward compatibility with earlier versions and for convenience when you don't implement a secured database, the Microsoft Access database engine automatically creates a default **Workspace** object when needed if one isn't already open. In this case, the **DefaultUser** and **DefaultPassword** property values define the user and password for the default **Workspace** object.

このプロパティを有効にするには、DAO メソッドを呼び出す前に設定する必要があります。

