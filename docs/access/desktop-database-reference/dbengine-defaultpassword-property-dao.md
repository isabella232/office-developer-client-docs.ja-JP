---
title: DBEngine.DefaultPassword プロパティ (DAO)
TOCTitle: DefaultPassword Property
ms:assetid: 189e34f3-d573-c75f-8be2-d98c50df8a52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845616(v=office.15)
ms:contentKeyID: 48543478
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 72e73d29129c749d5479e2c7b17827f13adb4847
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704736"
---
# <a name="dbenginedefaultpassword-property-dao"></a>DBEngine.DefaultPassword プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

既定の **Workspace** を作成するために初期化時に使用されるパスワードを設定します。値の取得および設定が可能です。文字列型 ( **String**) の値を使用します。

## <a name="syntax"></a>構文

*式*です。DefaultPassword

*式***DBEngine**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**DefaultPassword** の設定値は、最大 20 文字の文字列データ型 (String) です。このプロパティには、ASCII の 0 を除くすべての文字を含めることができます。


> [!NOTE]
> [!メモ] パスワードには、大文字、小文字、数字、記号を組み合わせた複雑なものを使用してください。これらの文字を混在させたものになっていないパスワードは強固とはいえません。たとえば、Y6dh!et5 は安全性の高いパスワードです。House27 は推測されやすいパスワードです。また、高い安全性を保ちながらも、書き留めておかなくても覚えておくことができるパスワードを使用してください。

既定では、 **DefaultUser** プロパティは "admin" に設定され、 **DefaultPassword** プロパティは長さが 0 の文字列 ("") に設定されます。

通常は、CreateWorkspace メソッドを使用して、任意のユーザー名とパスワードを持つ Workspace オブジェクトを作成します。ただし、以前のバージョンとの互換性を保つため、およびセキュリティで保護されたデータベースを実装しない場合に便宜を図るために、Workspace オブジェクトがまだ開いていなければ、必要に応じて既定の Workspace オブジェクトが自動的に作成されます。この場合、DefaultUser プロパティと DefaultPassword プロパティの値により、既定の Workspace オブジェクトのユーザーとパスワードが定義されます。

このプロパティを有効にするには、DAO メソッドを呼び出す前に設定する必要があります。

