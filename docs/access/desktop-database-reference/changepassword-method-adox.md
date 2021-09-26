---
title: ChangePassword メソッド (ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5fdc08b191e735ddcad0b9dae9962cb657521993
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590094"
---
# <a name="changepassword-method-adox"></a>ChangePassword メソッド (ADOX)

**適用先**: Access 2013、Office 2013

ユーザー アカウントのパスワードを変更します。

## <a name="syntax"></a>構文

*ユーザー 。* ChangePassword *OldPassword*, *NewPassword*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*OldPassword* |ユーザーの現在のパスワードを示す文字列型 (**String**) の値を指定します。ユーザーが現在パスワードを使用していない場合は、*OldPassword* に空の文字列 ("") を指定してください。|
|*NewPassword* |新しいパスワードを表す文字列型 ( **String** ) の値を指定します。|

## <a name="remarks"></a>注釈

セキュリティ上の理由から、新規パスワードに加え、古いパスワードを指定する必要があります。

プロバイダーがトラスティ プロパティの管理をサポートしていない場合は、エラーが発生します。

