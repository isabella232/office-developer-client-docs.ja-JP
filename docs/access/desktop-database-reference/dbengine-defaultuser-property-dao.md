---
title: DBEngine.DefaultUser プロパティ (DAO)
TOCTitle: DefaultUser Property
ms:assetid: 41ee0211-0794-6026-7341-3698a0b2c588
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192905(v=office.15)
ms:contentKeyID: 48544464
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053071
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 4b6a8a8f65b450d38a820bd00468cbde38facbd6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585817"
---
# <a name="dbenginedefaultuser-property-dao"></a>DBEngine.DefaultUser プロパティ (DAO)


**適用先**: Access 2013、Office 2013

既定の **Workspace** オブジェクトを作成するために初期化時に使用されるユーザー名を設定します。値の取得および設定が可能です。文字列型 ( **String**) の値を使用します。

## <a name="syntax"></a>構文

*式* .DefaultUser

*式* **DBEngine** オブジェクトを返す式。

## <a name="remarks"></a>注釈

The setting for **DefaultUser** is a String data type. これは、Microsoft Access ワークスペースでは 1 ~ 20 文字の長さであり、アルファベット文字、アクセント文字、数字、スペース、および記号を含めることができます(" (二重引用符)、/(スラッシュ)、(円記号)、(かっこ \\ \[ \] )、: (コロン)、|(パイプ), \< (less-than sign), \> (大きい符号), + (プラス記号), = (等号), ;(セミコロン)、、 ( コンマ)、? (疑問符 \* )、(アスタリスク)、先頭のスペース、および制御文字 (ASCII 00 ~ ASCII 31)。


> [!NOTE]
> [!メモ] パスワードには、大文字、小文字、数字、記号を組み合わせた複雑なものを使用してください。これらの文字を混在させたものになっていないパスワードは強固とはいえません。たとえば、Y6dh!et5 は安全性の高いパスワードです。House27 は推測されやすいパスワードです。また、高い安全性を保ちながらも、書き留めておかなくても覚えておくことができるパスワードを使用してください。

既定では、 **DefaultUser** プロパティは "admin" に設定され、 **DefaultPassword** プロパティは長さが 0 の文字列 ("") に設定されます。

通常は、ユーザー名は大文字と小文字を区別しませんが、削除された、または別のワークグループで作成されたユーザー アカウントを再作成する場合、ユーザー名と元の名前は、大文字と小文字の区別まで厳密に一致している必要があります。パスワードは大文字と小文字を区別します。

Typically, you use the **CreateWorkspace** method to create a **Workspace** object with a given user name and password. However, for backward compatibility with earlier versions and for convenience when you don't implement a secured database, the Microsoft Access database engine automatically creates a default **Workspace** object when needed if one isn't already open. In this case, the **DefaultUser** and **DefaultPassword** property values define the user and password for the default **Workspace** object.

このプロパティを有効にするには、DAO メソッドを呼び出す前に設定する必要があります。

