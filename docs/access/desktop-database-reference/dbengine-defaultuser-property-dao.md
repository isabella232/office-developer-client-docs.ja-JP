---
title: DBEngine ユーザープロパティ (DAO)
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
localization_priority: Normal
ms.openlocfilehash: c29f9663ce3591fe5b1633239e8ec0d8866ee16a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294348"
---
# <a name="dbenginedefaultuser-property-dao"></a>DBEngine ユーザープロパティ (DAO)


**適用先:** Access 2013、Office 2013

初期化されたときに、既定の**Workspace**オブジェクトを作成するために使用されるユーザー名を設定します。 値の取得および設定が可能です。

## <a name="syntax"></a>構文

*式*。DefaultUser

*式***DBEngine**オブジェクトを返すオブジェクト式を指定します。

## <a name="remarks"></a>注釈

The setting for **DefaultUser** is a String data type. Microsoft access ワークスペースでは 1 ~ 20 文字の長さにすることができます。また、: "(引用符),/(スラッシュ), \\ (円記号) \[ \] , (かっこ) のように、英数字、アクセント記号付きの文字、数字、スペース、記号を含めることができます。、: (コロン)、|(パイプ)、 \< (不等号)、 \> (不等号)、+ (正符号)、= (等号)、、、。(セミコロン)、、(コンマ)、? (疑問符)、 \* (アスタリスク)、先頭のスペース、制御文字 (ascii 00 ~ ascii 31)。


> [!NOTE]
> [!メモ] パスワードには、大文字、小文字、数字、記号を組み合わせた複雑なものを使用してください。これらの文字を混在させたものになっていないパスワードは強固とはいえません。たとえば、Y6dh!et5 は安全性の高いパスワードです。House27 は推測されやすいパスワードです。また、高い安全性を保ちながらも、書き留めておかなくても覚えておくことができるパスワードを使用してください。

既定では、 **DefaultUser** プロパティは "admin" に設定され、 **DefaultPassword** プロパティは長さが 0 の文字列 ("") に設定されます。

通常は、ユーザー名は大文字と小文字を区別しませんが、削除された、または別のワークグループで作成されたユーザー アカウントを再作成する場合、ユーザー名と元の名前は、大文字と小文字の区別まで厳密に一致している必要があります。パスワードは大文字と小文字を区別します。

Typically, you use the **CreateWorkspace** method to create a **Workspace** object with a given user name and password. However, for backward compatibility with earlier versions and for convenience when you don't implement a secured database, the Microsoft Access database engine automatically creates a default **Workspace** object when needed if one isn't already open. In this case, the **DefaultUser** and **DefaultPassword** property values define the user and password for the default **Workspace** object.

このプロパティを有効にするには、DAO メソッドを呼び出す前に設定する必要があります。

