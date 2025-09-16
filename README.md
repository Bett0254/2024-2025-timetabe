# HTML/CSS Timetable Project

A responsive and visually appealing weekly timetable built with HTML and CSS. Perfect for schools, students, or anyone who needs to organize their weekly schedule.

## Features

- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices
- **Color-Coded Subjects**: Each subject has its own distinct color for easy identification
- **Interactive Elements**: Hover effects on subject cells for better user experience
- **Print-Friendly**: Optimized styles for printing
- **Room Information**: Displays both subject and room/location details
- **Modern Styling**: Uses CSS gradients, shadows, and smooth transitions

## File Structure

```
timetable-project/
├── index.html          # Main HTML file containing the timetable structure
├── styles.css          # CSS file with all styling and responsive design
└── README.md          # This documentation file
```

## HTML Structure Overview

The timetable is built using semantic HTML with the following key elements:

### Basic Table Structure
```html
<table class="timetable">
    <thead>
        <tr>
            <th class="time-header">Time</th>
            <th>Monday</th>
            <!-- Other days... -->
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="time-slot">8:00 AM</td>
            <td class="subject math">Mathematics<br><span class="room">Room 101</span></td>
            <!-- Other subjects... -->
        </tr>
        <!-- More time slots... -->
    </tbody>
</table>
```

### CSS Class System

The timetable uses a comprehensive class system for styling:

#### Time-related Classes
- `.time-header` - Styles the "Time" column header
- `.time-slot` - Styles the time cells (8:00 AM, 9:00 AM, etc.)

#### Subject Classes
- `.subject` - Base class for all subject cells
- `.subject.math` - Mathematics (Red gradient)
- `.subject.english` - English (Teal gradient)
- `.subject.science` - Science (Blue gradient)
- `.subject.history` - History (Orange gradient)
- `.subject.pe` - Physical Education (Green gradient)
- `.subject.art` - Arts (Purple gradient)
- `.subject.music` - Music (Pink gradient)
- `.subject.computer` - Computer Science (Indigo gradient)
- `.subject.study` - Study Hall (Brown gradient)
- `.subject.free` - Free Period (Gray gradient)

#### Special Classes
- `.break` - Morning/afternoon breaks (Yellow gradient)
- `.lunch` - Lunch break (Light green gradient)
- `.end` - End of day marker (Brown gradient)
- `.room` - Room/location information styling

## Customization Guide

### Adding New Subjects

1. **HTML**: Add the subject cell with appropriate class
```html
<td class="subject newsubject">New Subject<br><span class="room">Room 999</span></td>
```

2. **CSS**: Add the color scheme
```css
.subject.newsubject {
    background: linear-gradient(135deg, #color1, #color2);
    color: white;
}

.legend-item.newsubject {
    background: linear-gradient(135deg, #color1, #color2);
}
```

3. **Legend**: Add to the legend section
```html
<span class="legend-item newsubject">New Subject</span>
```

### Modifying Colors

Each subject uses CSS gradients. To change colors, modify the `background` property:

```css
.subject.math {
    background: linear-gradient(135deg, #your-color-1, #your-color-2);
    color: white; /* or black for better contrast */
}
```

### Changing Time Slots

To modify time slots:

1. Update the time in the `.time-slot` cell
2. Adjust the corresponding subject cells
3. Add or remove rows as needed

### Responsive Breakpoints

The CSS includes three responsive breakpoints:

- **768px and below**: Tablet styles
- **480px and below**: Mobile styles
- **Print**: Print-optimized styles

## Browser Compatibility

This timetable works in all modern browsers including:
- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## Usage Instructions

1. **Basic Usage**: Open `index.html` in any web browser
2. **Customization**: Edit the HTML content and CSS styles as needed
3. **Printing**: Use browser's print function (Ctrl+P) for a print-friendly version
4. **Mobile**: The design automatically adapts to smaller screens

## Advanced Customization

### Adding More Days

To add weekend days:

1. Add new `<th>` headers for Saturday/Sunday
2. Add corresponding `<td>` cells in each row
3. Adjust CSS grid/responsive styles if needed

### Creating Multiple Timetables

You can create multiple timetables by:

1. Duplicating the table structure
2. Using unique IDs or classes
3. Adding navigation between different timetables

### JavaScript Integration

While this is a pure HTML/CSS solution, you can enhance it with JavaScript for:

- Dynamic schedule loading
- Interactive editing
- Data export/import
- Calendar integration

## License

This project is open source and available under the MIT License. Feel free to use, modify, and distribute as needed.

## Contributing

Feel free to submit issues and pull requests to improve the timetable design and functionality.