# Angular Animations Examples

## *ngFor
### MatItem
<div align="center"><img src="todo2.gif" width="400px" /></div>
```javascript
trigger('matListAnim', [
      transition('* <=> *', [
        query('mat-list-item:enter',
          [
            style({ opacity: 0, transform: 'translateY(-15px)' }),
            stagger(
              '100ms',
              animate(
                '500ms ease-out',
                style({ opacity: 1, transform: 'translateY(0px)' })
              )
            )
          ],
          {optional: true}
        )
      ])
    ])
```

### MatCards
<div align="center"><img src="stats.gif" heigth="200px" /></div>
```javascript
trigger('matCardsAnim', [
      transition('* <=> *', [
        query('mat-card:enter',
          [style({opacity: 0}), stagger('200ms', animate('600ms ease-out', style({opacity: 1})))],
          {optional: true}
        ),
        query('mat-card:leave',
          animate('200ms', style({opacity: 0})),
          {optional: true}
        )
      ])
    ])
```
