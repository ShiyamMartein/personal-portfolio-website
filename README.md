int choice;
do {
    printf("\nPersonal Portfolio Manager\n");
    printf("1. Add Project\n");
    printf("2. View Projects\n");
    printf("3. Add Skill\n");
    printf("4. View Skills\n");
    printf("5. Exit\n");
    printf("Enter your choice: ");
    scanf("%d", &choice);
    getchar(); // Consume the newline character

    switch (choice) {
        case 1:
            addProject(projects, &projectCount);
            break;
        case 2:
            viewProjects(projects, projectCount);
            break;
        case 3:
            addSkill(skills, &skillCount);
            break;
        case 4:
            viewSkills(skills, skillCount);
            break;
        case 5:
            printf("Exiting...\n");
            break;
        default:
            printf("Invalid choice. Please try again.\n");
    }
} while (choice != 5);
