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
ms.openlocfilehash: 4f7179b6cb6dc442775082474039ab61831cb627
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867693"
---
# <a name="dbenginedefaultuser-property-dao"></a>DBEngine.DefaultUser プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

既定の **Workspace** オブジェクトを作成するために初期化時に使用されるユーザー名を設定します。値の取得および設定が可能です。文字列型 ( **String**) の値を使用します。

## <a name="syntax"></a>構文

*式*です。デフォルト

*式***DBEngine**オブジェクトを返すオブジェクト式を指定します。

## <a name="remarks"></a>注釈

**デフォルト**の設定は、文字列データ型です。 1 ~ 20 文字であることができます Microsoft Access では長い間ワークスペースとして含めることができますアルファベット文字、アクセント記号付き文字、数字、スペース、および記号:"(引用符は含みません)、/(スラッシュ)、 \\ (バック スラッシュ)、 \[ \] (角かっこ)、: (コロン)、|(パイプ)、 \< (以下の記号よりも)、 \> (大きい-記号よりも)、+ (プラス記号)、= (等しい記号)、です。(セミコロン)、(コンマ)、でしょうか。 (疑問符 ())、 \* (アスタリスク)、先頭のスペース、および制御文字 (ASCII 00 ASCII 31)。


> [!NOTE]
> [!メモ] パスワードには、大文字、小文字、数字、記号を組み合わせた複雑なものを使用してください。これらの文字を混在させたものになっていないパスワードは強固とはいえません。たとえば、Y6dh!et5 は安全性の高いパスワードです。House27 は推測されやすいパスワードです。また、高い安全性を保ちながらも、書き留めておかなくても覚えておくことができるパスワードを使用してください。

既定では、 **DefaultUser** プロパティは "admin" に設定され、 **DefaultPassword** プロパティは長さが 0 の文字列 ("") に設定されます。

通常は、ユーザー名は大文字と小文字を区別しませんが、削除された、または別のワークグループで作成されたユーザー アカウントを再作成する場合、ユーザー名と元の名前は、大文字と小文字の区別まで厳密に一致している必要があります。パスワードは大文字と小文字を区別します。

通常は、CreateWorkspace メソッドを使用して、任意のユーザー名とパスワードを持つ Workspace オブジェクトを作成します。ただし、以前のバージョンとの互換性を保つため、およびセキュリティで保護されたデータベースを実装しない場合に便宜を図るために、Workspace オブジェクトがまだ開いていなければ、必要に応じて既定の Workspace オブジェクトが自動的に作成されます。この場合、DefaultUser プロパティと DefaultPassword プロパティの値により、既定の Workspace オブジェクトのユーザーとパスワードが定義されます。

このプロパティを有効にするには、DAO メソッドを呼び出す前に設定する必要があります。

