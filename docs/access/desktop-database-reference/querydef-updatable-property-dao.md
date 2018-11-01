---
title: QueryDef.Updatable プロパティ (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4ad761c2941cb556ce67c9f716247663220f753f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873692"
---
# <a name="querydefupdatable-property-dao"></a>QueryDef.Updatable プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

DAO オブジェクトを変更できるかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( **Boolean**) の値を使用します。

## <a name="syntax"></a>構文

*式*です。更新可能です

*式***クエリ定義**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

クエリ結果の ****Recordset**** オブジェクトを更新できないときでも、クエリ定義を更新できる場合、 **QueryDef** オブジェクトの [Updatable](recordset-object-dao.md) プロパティは **True** に設定されます。

