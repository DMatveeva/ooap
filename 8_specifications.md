```
public abstract class Matrix {

    //запросы

    //предусловие: матрица непустая
    public abstract boolean containsFigures();

    //предусловие: матрица непустая
    public abstract Figures getFigures();

    //команды

    //предусловие: есть пустые клетки
    //постусловие: все клетки заполнены
    public abstract void fillEmptyCells();

    //предусловие: from и to находятся внутри матрицы
    //постусловие: значения в клетах поменялись местами
    public abstract void swapCells(Coordinate from, Coordinate to);

    //предусловие: figures находятся внутри матрицы
    //постусловие: figures пустые
    public abstract void cleanFigures(Figures figures);

    //постусловие: матрица очищена
    public abstract void clear();
}

public abstract class Figure {

    //команды

    //постусловие: фигура очищена
    public abstract void clean();
}

public abstract class Cell {

    // создает Cell c координатой
    public Cell (Coordinate coordinate) {

    }

    //запросы

    public abstract boolean isEmpty();

    // команды

    //предусловие: other != this
    //постусловие: значение в клетках поменялись местами
    public abstract void update(Cell other);
}

public abstract class BonusAccount {

    // команды
    public abstract Bonus getBonuses();

    // запросы

    // предусловие: bonus > zero
    public abstract void add(Bonus bonus);

    public abstract void setStrategy(BonusStrategy strategy);
}
```
