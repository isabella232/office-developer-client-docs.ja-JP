---
title: 分類項目を列挙および追加する
TOCTitle: Enumerate and add categories
ms:assetid: 17a94a01-c463-4332-851e-7d280c66d8c2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424467(v=office.15)
ms:contentKeyID: 55119829
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 27fc8630c8e2eb0b491dbb5075f4c58aacec7f93
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406247"
---
# <a name="enumerate-and-add-categories"></a>分類項目を列挙および追加する

この例では、分類項目を列挙し、メイン分類項目リストに分類項目を追加する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

Outlook のオブジェクト モデルは、ユーザーの受信トレイのアイテムを整理しやすくするための分類項目をサポートしています。高レベルな整理を維持するために、以下を行うことができます。

- Outlook アイテムを分類し、分類項目ごとに表示します。
- 単一の Outlook アイテムに複数の色の分類項目を適用します。
- 色の分類項目により Outlook アイテムのグループ化と並べ替えを行います。
- 色の分類項目のそれぞれにショートカット キーを割り当てて、ユーザーがアイテムを分類しやすくします。
- プログラムにより、または Outlook のユーザー インターフェイスでのユーザー操作により、色の分類項目を作成、削除、および変更します。

Outlook オブジェクト モデルでは、分類項目の機能が利用できるように、メイン分類項目リスト内の単一のユーザー定義の色の分類項目を表す [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) オブジェクトが提供されます。 メイン分類項目リストには、Outlook のユーザー インターフェイスに表示される色の分類項目が含まれます。 このリストは [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) オブジェクトの [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) コレクションで表されます。 **Category** オブジェクトを作成するには、**Categories** コレクションの [Add(String, Object, Object)](https://msdn.microsoft.com/library/bb623093\(v=office.15\)) メソッドを使用します。 **Category** オブジェクトを作成すると、変更をすることができないグローバル一意識別子 (GUID) が作成されます。 GUID は、[CategoryID](https://msdn.microsoft.com/library/bb647100\(v=office.15\)) プロパティに表されます。 ただし、**Category** オブジェクトの [Name](https://msdn.microsoft.com/library/bb645577\(v=office.15\))、[Color](https://msdn.microsoft.com/library/bb612316\(v=office.15\))、および [ShortcutKey](https://msdn.microsoft.com/library/bb644944\(v=office.15\)) プロパティの設定をすると、色の分類項目と関連付けられた名前、色、およびショートカット キーをそれぞれ変更することができます。 **Color** プロパティを変更するには、そのプロパティの [OlCategoryColor](https://msdn.microsoft.com/library/bb608974\(v=office.15\))定数の設定または取得をします。 カスタム コントロールで色を再現するは、以下の、**Category** オブジェクトの読み取り専用のプロパティを使用します。

  - [CategoryBorderColor](https://msdn.microsoft.com/library/bb610083\(v=office.15\))

  - [CategoryGradientBottomColor](https://msdn.microsoft.com/library/bb647357\(v=office.15\))

  - [CategoryGradientTopColor](https://msdn.microsoft.com/library/bb623975\(v=office.15\))

これらのプロパティは **OLE\_COLOR** 値を返します。この値は、**Category** オブジェクトの **Color** プロパティに依存します。

Outlook アイテムは分類項目名に基づいて表示されます。 各項目のオブジェクトには、分類項目名を表すコンマ区切り文字列を格納した **Categories** プロパティが含まれます。 (たとえば、[MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) オブジェクトでは、**MailItem** の [Categories](https://msdn.microsoft.com/library/bb646442\(v=office.15\)) プロパティを使用します)。 これにより、メインの分類項目リストにない分類項目もアイテムに追加することができます。


> [!NOTE]
> [!メモ] アイテムの **Categories** プロパティに、 **NameSpace** オブジェクトの **Categories** コレクションにない分類項目名が含まれている場合、Outlook アイテムに関連付けられたその分類項目名は表示されますが、関連付けられた色はありません。 **Item** オブジェクトの **Categories** プロパティは **Categories** コレクションを返しません。

次のコード例で、最初のプロシージャである olCatlist では、**Categories** コレクションが表す現在のユーザーのメイン分類項目リストを取得します。 次に、そのコレクションの **Category** オブジェクトに対して順に処理を行い、 **Name** プロパティおよび **CategoryID** プロパティを [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクションのトレース リスナーに書き込みます。 2 番目のプロシージャの AddACategory では、現在のユーザーのメイン分類項目リストを取得し、CategoryExists メソッドを使用して "ISV" という名前の分類項目がコレクションに存在するかどうかを確認します。 "ISV" という名前の分類項目が存在しない場合、AddACategory は、**Categories** コレクションの **Add** メソッドを使用して、分類項目のメイン リストに "ISV" という名前の分類項目を追加し、濃い青色を割り当てます。 また、この分類項目のショートカット キーに Ctrl + F11 を割り当てます。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateCategories()
{
    Outlook.Categories categories =
        Application.Session.Categories;
    foreach (Outlook.Category category in categories)
    {
        Debug.WriteLine(category.Name);
        Debug.WriteLine(category.CategoryID);
    }
}

private void AddACategory()
{
    Outlook.Categories categories =
        Application.Session.Categories;
    if (!CategoryExists("ISV"))
    {
        Outlook.Category category = categories.Add("ISV",
            Outlook.OlCategoryColor.olCategoryColorDarkBlue,
            Outlook.OlCategoryShortcutKey.olCategoryShortcutKeyCtrlF11);
    }
}

private bool CategoryExists(string categoryName)
{
    try
    {
        Outlook.Category category = 
            Application.Session.Categories[categoryName];
        if(category != null)
        {
            return true;
        }
        else
        {
            return false;
        }
    }
    catch { return false; }
}
```

## <a name="see-also"></a>関連項目

- [色の分類項目](color-categories.md)

