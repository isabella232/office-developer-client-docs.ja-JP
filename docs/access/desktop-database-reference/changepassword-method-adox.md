---
title: ChangePassword メソッド (ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7eef5fc93f9cce68e6342b62c1ab07ee6f65587f
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946021"
---
# <a name="changepassword-method-adox"></a>ChangePassword メソッド (ADOX)


**適用されます**Access 2013、Office 2013。



ユーザー アカウントのパスワードを変更します。

## <a name="syntax"></a>構文

*ユーザー*です。パスワードの変更を*OldPassword*、 *NewPassword*

## <a name="parameters"></a>パラメーター

- *OldPassword*

  - ユーザーの現在のパスワードを示す文字列型 (**String**) の値を指定します。ユーザーが現在パスワードを使用していない場合は、*OldPassword* に空の文字列 ("") を指定してください。

- *NewPassword*

  - 新しいパスワードを表す文字列型 ( **String** ) の値を指定します。

## <a name="remarks"></a>解説

セキュリティ上の理由から、新規パスワードに加え、古いパスワードを指定する必要があります。

プロバイダーがトラスティ プロパティの管理をサポートしていない場合は、エラーが発生します。

