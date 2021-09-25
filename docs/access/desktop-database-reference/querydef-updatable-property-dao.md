---
title: QueryDef.Updatable プロパティ (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5557e61a12d8db8c5532a547778540e4db5ac9ed
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565010"
---
# <a name="querydefupdatable-property-dao"></a>QueryDef.Updatable プロパティ (DAO)


**適用先:** Access 2013、Office 2013

DAO オブジェクトを変更できるかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( **Boolean** ) の値を使用します。  

## <a name="syntax"></a>構文

*式* .更新可能

*式* **QueryDef** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

クエリ結果の **[Recordset](recordset-object-dao.md)** オブジェクトを更新できないときでも、クエリ定義を更新できる場合、**QueryDef** オブジェクトの **Updatable** プロパティは **True** に設定されます。

